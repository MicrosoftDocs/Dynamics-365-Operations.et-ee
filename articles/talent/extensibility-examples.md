---
title: Talenti laiendamine PowerAppsi ja Microsoft Flow’ga – näidisstsenaariumid
description: Selles teemas kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 for Talent, mis kasutab Microsoft PowerAppsi ja Microsoft Flow’d.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c113b0f4ab2c8e44d00fcfca3f0a6ca828a854ae
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517784"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="b9fb6-103">Talenti laiendamine PowerAppsi ja Microsoft Flow’ga – näidisstsenaariumid</span><span class="sxs-lookup"><span data-stu-id="b9fb6-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="b9fb6-104">Selles teemas kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 for Talent, mis kasutab Microsoft PowerAppsi ja Microsoft Flow’d.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="b9fb6-105">Saate PowerAppsi keskkonda importida iga näitega seotud lahendusepaketi.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="b9fb6-106">Seejärel saate pakette kasutada juhisena või lähtekohana teie organisatsioonile sobivate stsenaariumide rakendamiseks.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9fb6-107">Kui soovite kasutada selles teemas kirjeldatud malle ja rakendust muutmata kujul, katsetage neid kindlasti veendumaks, et need hõlmavad kõiki teie juurutusele kehtivaid stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="b9fb6-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="b9fb6-108">Prerequisites</span></span>

- <span data-ttu-id="b9fb6-109">Pakettide importimiseks peab kasutajatel olema **keskkonna looja** luba.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="b9fb6-110">Rakenduste eksportimiseks või importimiseks peab kasutajatel olema PowerAppsi plaani 2 litsents või PowerAppsi plaani 2 proovilitsents.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="b9fb6-111">Flow ja Formi ühendamine</span><span class="sxs-lookup"><span data-stu-id="b9fb6-111">Flow – Form Connect</span></span>

<span data-ttu-id="b9fb6-112">Malli **Flow ja Formi ühendamine** saab kasutada andmete lugemiseks Microsoft Formsist ja nende salvestamiseks teenuse Common Data Service üksusesse.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="b9fb6-113">Seda malli saab laiendada, et seda saaks kasutada ka teistes stsenaariumites.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="b9fb6-114">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-114">Here are some examples:</span></span>

- <span data-ttu-id="b9fb6-115">Kandidaadi hinnangute jäädvustamine.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="b9fb6-116">Kursuse küsimustike tulemuste jäädvustamine.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="b9fb6-117">Töövestluse küsimuste teegi koostamine inimressursside (HR) administraatorite jaoks.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="b9fb6-118">Kandidaadi hinnangu jäädvustamine vestluse protsessi kohta</span><span class="sxs-lookup"><span data-stu-id="b9fb6-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="b9fb6-119">Microsoft Dynamics 365: Attractis saab vorme kuvada kandidaadi portaalis ja kandidaadid saavad täita üksikasju.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="b9fb6-120">Vorme saab ka tegevustena töömalli manustada.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="b9fb6-121">Kui kandidaat vormi esitab, jäädvustab Microsoft Flow vormi esitamise, loeb andmeid ja salvestab need teenuse Common Data Service üksusesse.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="b9fb6-122">Malli **Flow ja Formi ühendamine** ja kohandatud üksuse struktuuri alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Flow ja Formi ühendamine](https://go.microsoft.com/fwlink/?linkid=2081988).</span><span class="sxs-lookup"><span data-stu-id="b9fb6-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="b9fb6-123">Powerappsi edastatud parameetrite käivitamine ja ekstraktimine</span><span class="sxs-lookup"><span data-stu-id="b9fb6-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="b9fb6-124">Malli **Powerappsi edastatud parameetrite käivitamine ja ekstraktimine** saab kasutada lähtekohana mis tahes PowerAppsi stsenaariumi jaoks, mis on omane Attractile.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="b9fb6-125">See sisaldab kõiki vaikeparameetreid, mille Attract edastab, nt **Tööavaldus**, **Kandidaadi ID** ja **Töö ID**.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="b9fb6-126">Seda malli saab kasutada kandidaadi hinnanguvormi leidmiseks, et personalijuht saaks kandidaadi täidetud hinnangut vaadata.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="b9fb6-127">PowerAppsiga loodud rakendusi saab manustada Attractis töömalli.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="b9fb6-128">Malli **Powerappsi edastatud parameetrite käivitamine ja ekstraktimine** ja kohandatud üksuse struktuuri alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Powerappsi edastatud parameetrite käivitamine ja ekstraktimine](https://go.microsoft.com/fwlink/?linkid=2081991).</span><span class="sxs-lookup"><span data-stu-id="b9fb6-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="b9fb6-129">Office 365-iga integreerimine</span><span class="sxs-lookup"><span data-stu-id="b9fb6-129">Integration with Office 365</span></span>

<span data-ttu-id="b9fb6-130">Rakendust **Office 365-ga integreerimine** saab kasutada sisse logitud kasutajate töörühma teabe ekstraktimiseks Microsoft Office 365-st.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="b9fb6-131">See viitab töötajatele Talentis, et ekstraktida sisse- ja väljaregistreerimiste üksikasju ning erandite kirjeid.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="b9fb6-132">Sisse- ja väljaregistreerimiste üksikasju salvestatakse teenuse Common Data Service kohandatud üksustes.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="b9fb6-133">Eeldus on, et need üksikasjad täidab muude tootjate süsteemid integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="b9fb6-134">Seda rakendust saab laiendada, et seda saaks kasutada ka teistes stsenaariumites.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="b9fb6-135">Näiteks saab seda kasutada töörühma puhkuste teabe, kalendrisündmuste ja töörühmaga seotud sündmuste näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="b9fb6-136">Rakenduse **Office 365-ga integreerimine** ja kohandatud üksuse struktuuri alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Office 365-ga integreerimine](https://go.microsoft.com/fwlink/?linkid=2081787).</span><span class="sxs-lookup"><span data-stu-id="b9fb6-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="b9fb6-137">Flow – meiliteatis</span><span class="sxs-lookup"><span data-stu-id="b9fb6-137">Flow – Email Notification</span></span>

<span data-ttu-id="b9fb6-138">Malli **Flow – meiliteatis** saab kasutada meiliteatise stsenaariumide jaoks.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="b9fb6-139">Seda saab kasutada teavitusmeilide saatmiseks kandidaatidele, kelle värbamistöörühm värbamisprotsessi mis tahes etapis tagasi lükkab.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="b9fb6-140">Seda malli saab laiendada, et see jälgiks muudatusi kandidaadi etapis kogu värbamisprotsessi jooksul ning saadaks teatisi värbamistöörühmale ja kandidaadile.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="b9fb6-141">Üldiselt saab lahenduses Common Data Service salvestatud üksuste jaoks voogusid seadistada nii, et need saadavad teatisi rakenduse Core HR, Attract või Dynamics 365 Talent: Onboard sündmuste kohta.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="b9fb6-142">Malli **Flow – meiliteatis** alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Flow – meiliteatis](https://go.microsoft.com/fwlink/?linkid=2082103).</span><span class="sxs-lookup"><span data-stu-id="b9fb6-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="b9fb6-143">Flow – SQL-i ühendamine ja käivitamine</span><span class="sxs-lookup"><span data-stu-id="b9fb6-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="b9fb6-144">Mall **Flow – SQL-i ühendamine ja käivitamine** loob ühenduse Microsoft SQL Serveriga ja lubab käivitada SQL-i päringuid.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="b9fb6-145">Kuigi see mall on mõeldud lugema ja värskendama SQL-i tabeleid, saab seda laiendada kasutamiseks teistes stsenaariumites.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="b9fb6-146">Näiteks saab seda kasutada vahetabeli täitmiseks teenuses Common Data Service kirjetega SQL Serverist ja vahetabeli aeg-ajalt sünkroonimiseks, kasutades SQL Serveri astmelist jaotust.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="b9fb6-147">Malli **Flow – SQL-i ühendamine ja käivitamine** alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Flow – SQL-i ühendamine ja käivitamine](https://go.microsoft.com/fwlink/?linkid=2081789).</span><span class="sxs-lookup"><span data-stu-id="b9fb6-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="b9fb6-148">Flow – SharePointi integreerimine</span><span class="sxs-lookup"><span data-stu-id="b9fb6-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="b9fb6-149">Malli **Flow – SharePointi integreerimine** saab kasutada andmete lugemiseks Microsoft SharePointi loendist, loendi võrdlemiseks teenuse Common Data Service mis tahes üksuse väljaväärtustega ja võrdluse tulemuste saatmiseks teavitusmeilina.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="b9fb6-150">Organisatsioonil võivad olla oskused, mida tal on tingimata vaja.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="b9fb6-151">Neid oskusi saab hoiustada SharePointis SharePointi loendina.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="b9fb6-152">Kui kandidaat kandideerib mis tahes tööle, mille kohta on olemas vajalike oskuste loend, ning kandidaadi oskuse ja SharePointi salvestatud oskuste vahel on oluline kokkulangevus, saadetakse selle kohta teavitusmeil.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="b9fb6-153">Nii täidetakse kiiresti vajaminevad ametikohad kiiremini, kuna teatised aitavad värbajatel jõuda kõigi organisatsiooni kandidaatideni ja neid värvata.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="b9fb6-154">Seda malli saab laiendada kasutamiseks mis tahes stsenaariumi jaoks, mis hõlmab SharePointi integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="b9fb6-155">Malli **Flow – SharePointi integratsioon** alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Flow – SharePointi integratsioon](https://go.microsoft.com/fwlink/?linkid=2082109).</span><span class="sxs-lookup"><span data-stu-id="b9fb6-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="admin-console-to-manage-talent-pools"></a><span data-ttu-id="b9fb6-156">Administraatori konsool talendikaustade haldamiseks</span><span class="sxs-lookup"><span data-stu-id="b9fb6-156">Admin console to manage talent pools</span></span>

<span data-ttu-id="b9fb6-157">Kui lubate integratsiooni LinkedIniga, loob Attract automaatselt LinkedIni talentikausta.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-157">When you enable integration with LinkedIn, Attract automatically createas a LinkedIn talent pool.</span></span> <span data-ttu-id="b9fb6-158">Kui värbaja saadab InMail kandidaadile LinkedIni kaudu, loob Attract kandidaadile profiili ja temast saab LinkedIni talendikausta liige.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-158">When a recruiter exchanges InMail with a recruit through LinkedIn, Attract creates a profile for the recruit, and the recruit becomes a member of the LinkedIn talent pool.</span></span> <span data-ttu-id="b9fb6-159">See PowerAppsi rakendus on otstarbekas kandidaatide järjestamiseks talendikaustades oskuste alusel.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-159">This PowerApps app is useful for reorganizing candidates in talent pools based on skill.</span></span>

<span data-ttu-id="b9fb6-160">Käivitage rakendus PowerApps administraatori konsoolina järgmiste ülesannete täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-160">Run this PowerApps app as an admin console to perform the following tasks:</span></span>

- <span data-ttu-id="b9fb6-161">Kandidaatide järjestamine talendikaustas</span><span class="sxs-lookup"><span data-stu-id="b9fb6-161">List candidates in a talent pool</span></span>
- <span data-ttu-id="b9fb6-162">Kandidaatide lisamine ja eemaldamine talendikausta</span><span class="sxs-lookup"><span data-stu-id="b9fb6-162">Add and remove candidates from a talent pool</span></span>
- <span data-ttu-id="b9fb6-163">Kandidaatide teisaldamine ühest talendikaustast teise</span><span class="sxs-lookup"><span data-stu-id="b9fb6-163">Move candidates from one talent pool to another</span></span>
- <span data-ttu-id="b9fb6-164">Määratlemine, kas kandidaadid on enne teisaldamist juba talendikaustas</span><span class="sxs-lookup"><span data-stu-id="b9fb6-164">Determine whether candidates are already part of a talent pool before moving them</span></span>
- <span data-ttu-id="b9fb6-165">Kandidaatide oskuste kontrollimine enne nende teisaldamist teistesse talendikaustadesse</span><span class="sxs-lookup"><span data-stu-id="b9fb6-165">Check the skills of candidates before moving them to other talent pools</span></span>

<span data-ttu-id="b9fb6-166">See PowerAppsi rakendus kasutab mitu-mitmele-seoseid ning saate seda kasutada mallina muudel juhtudel, kui teil on vaja ekstraktida kirjeid, millel on mitu-mitmele seosed.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-166">This PowerApps app uses many-to-many relationships, so you can use it as a template for other scenarios where you need to extract records that have many-to-many relationships.</span></span>

<span data-ttu-id="b9fb6-167">Malli **Administraatori konsool talendikaustade haldamiseks** allalaadimiseks avage [Administraatori konsool talendikaustade haldamiseks](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) Microsofti allalaadimiskeskuses.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-167">To download the **Admin console to manage talent pools** template,  go to [Admin console to manage talent pools](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9fb6-168">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b9fb6-168">Additional resources</span></span>

[<span data-ttu-id="b9fb6-169">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="b9fb6-169">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="b9fb6-170">Rakenduse ülekandmine rentnike ja keskkondade vahel</span><span class="sxs-lookup"><span data-stu-id="b9fb6-170">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
