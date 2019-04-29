---
title: Talenti laiendamine PowerAppsi ja Microsoft Flow’ga – näidisstsenaariumid
description: Selles teemas kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 for Talent, mis kasutab Microsoft PowerAppsi ja Microsoft Flow’d.
author: negudava
manager: Annbe
ms.date: 03/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 0aa3578047b9397682a7039d0dbcc05cc1b167e4
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/12/2019
ms.locfileid: "949916"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="07407-103">Talenti laiendamine PowerAppsi ja Microsoft Flow’ga – näidisstsenaariumid</span><span class="sxs-lookup"><span data-stu-id="07407-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="07407-104">Selles teemas kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 for Talent, mis kasutab Microsoft PowerAppsi ja Microsoft Flow’d.</span><span class="sxs-lookup"><span data-stu-id="07407-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="07407-105">Saate PowerAppsi keskkonda importida iga näitega seotud lahendusepaketi.</span><span class="sxs-lookup"><span data-stu-id="07407-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="07407-106">Seejärel saate pakette kasutada juhisena või lähtekohana teie organisatsioonile sobivate stsenaariumide rakendamiseks.</span><span class="sxs-lookup"><span data-stu-id="07407-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07407-107">Kui soovite kasutada selles teemas kirjeldatud malle ja rakendust muutmata kujul, katsetage neid kindlasti veendumaks, et need hõlmavad kõiki teie juurutusele kehtivaid stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="07407-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="07407-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="07407-108">Prerequisites</span></span>

- <span data-ttu-id="07407-109">Pakettide importimiseks peab kasutajatel olema **keskkonna looja** luba.</span><span class="sxs-lookup"><span data-stu-id="07407-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="07407-110">Rakenduste eksportimiseks või importimiseks peab kasutajatel olema PowerAppsi plaani 2 litsents või PowerAppsi plaani 2 proovilitsents.</span><span class="sxs-lookup"><span data-stu-id="07407-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="07407-111">Flow ja Formi ühendamine</span><span class="sxs-lookup"><span data-stu-id="07407-111">Flow – Form Connect</span></span>

<span data-ttu-id="07407-112">Malli **Flow ja Formi ühendamine** saab kasutada andmete lugemiseks Microsoft Formsist ja nende salvestamiseks teenuse Common Data Service üksusesse.</span><span class="sxs-lookup"><span data-stu-id="07407-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="07407-113">Seda malli saab laiendada, et seda saaks kasutada ka teistes stsenaariumites.</span><span class="sxs-lookup"><span data-stu-id="07407-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="07407-114">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="07407-114">Here are some examples:</span></span>

- <span data-ttu-id="07407-115">Kandidaadi hinnangute jäädvustamine.</span><span class="sxs-lookup"><span data-stu-id="07407-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="07407-116">Kursuse küsimustike tulemuste jäädvustamine.</span><span class="sxs-lookup"><span data-stu-id="07407-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="07407-117">Töövestluse küsimuste teegi koostamine inimressursside (HR) administraatorite jaoks.</span><span class="sxs-lookup"><span data-stu-id="07407-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="07407-118">Kandidaadi hinnangu jäädvustamine vestluse protsessi kohta</span><span class="sxs-lookup"><span data-stu-id="07407-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="07407-119">Microsoft Dynamics 365: Attractis saab vorme kuvada kandidaadi portaalis ja kandidaadid saavad täita üksikasju.</span><span class="sxs-lookup"><span data-stu-id="07407-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="07407-120">Vorme saab ka tegevustena töömalli manustada.</span><span class="sxs-lookup"><span data-stu-id="07407-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="07407-121">Kui kandidaat vormi esitab, jäädvustab Microsoft Flow vormi esitamise, loeb andmeid ja salvestab need teenuse Common Data Service üksusesse.</span><span class="sxs-lookup"><span data-stu-id="07407-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="07407-122">Malli **Flow ja Formi ühendamine** ja kohandatud üksuse struktuuri alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Flow ja Formi ühendamine](https://go.microsoft.com/fwlink/?linkid=2081988).</span><span class="sxs-lookup"><span data-stu-id="07407-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="07407-123">Powerappsi edastatud parameetrite käivitamine ja ekstraktimine</span><span class="sxs-lookup"><span data-stu-id="07407-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="07407-124">Malli **Powerappsi edastatud parameetrite käivitamine ja ekstraktimine** saab kasutada lähtekohana mis tahes PowerAppsi stsenaariumi jaoks, mis on omane Attractile.</span><span class="sxs-lookup"><span data-stu-id="07407-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="07407-125">See sisaldab kõiki vaikeparameetreid, mille Attract edastab, nt **Tööavaldus**, **Kandidaadi ID** ja **Töö ID**.</span><span class="sxs-lookup"><span data-stu-id="07407-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="07407-126">Seda malli saab kasutada kandidaadi hinnanguvormi leidmiseks, et personalijuht saaks kandidaadi täidetud hinnangut vaadata.</span><span class="sxs-lookup"><span data-stu-id="07407-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="07407-127">PowerAppsiga loodud rakendusi saab manustada Attractis töömalli.</span><span class="sxs-lookup"><span data-stu-id="07407-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="07407-128">Malli **Powerappsi edastatud parameetrite käivitamine ja ekstraktimine** ja kohandatud üksuse struktuuri alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Powerappsi edastatud parameetrite käivitamine ja ekstraktimine](https://go.microsoft.com/fwlink/?linkid=2081991).</span><span class="sxs-lookup"><span data-stu-id="07407-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="07407-129">Office 365-iga integreerimine</span><span class="sxs-lookup"><span data-stu-id="07407-129">Integration with Office 365</span></span>

<span data-ttu-id="07407-130">Rakendust **Office 365-ga integreerimine** saab kasutada sisse logitud kasutajate töörühma teabe ekstraktimiseks Microsoft Office 365-st.</span><span class="sxs-lookup"><span data-stu-id="07407-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="07407-131">See viitab töötajatele Talentis, et ekstraktida sisse- ja väljaregistreerimiste üksikasju ning erandite kirjeid.</span><span class="sxs-lookup"><span data-stu-id="07407-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="07407-132">Sisse- ja väljaregistreerimiste üksikasju salvestatakse teenuse Common Data Service kohandatud üksustes.</span><span class="sxs-lookup"><span data-stu-id="07407-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="07407-133">Eeldus on, et need üksikasjad täidab muude tootjate süsteemid integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="07407-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="07407-134">Seda rakendust saab laiendada, et seda saaks kasutada ka teistes stsenaariumites.</span><span class="sxs-lookup"><span data-stu-id="07407-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="07407-135">Näiteks saab seda kasutada töörühma puhkuste teabe, kalendrisündmuste ja töörühmaga seotud sündmuste näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="07407-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="07407-136">Rakenduse **Office 365-ga integreerimine** ja kohandatud üksuse struktuuri alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Office 365-ga integreerimine](https://go.microsoft.com/fwlink/?linkid=2081787).</span><span class="sxs-lookup"><span data-stu-id="07407-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="07407-137">Flow – meiliteatis</span><span class="sxs-lookup"><span data-stu-id="07407-137">Flow – Email Notification</span></span>

<span data-ttu-id="07407-138">Malli **Flow – meiliteatis** saab kasutada meiliteatise stsenaariumide jaoks.</span><span class="sxs-lookup"><span data-stu-id="07407-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="07407-139">Seda saab kasutada teavitusmeilide saatmiseks kandidaatidele, kelle värbamistöörühm värbamisprotsessi mis tahes etapis tagasi lükkab.</span><span class="sxs-lookup"><span data-stu-id="07407-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="07407-140">Seda malli saab laiendada, et see jälgiks muudatusi kandidaadi etapis kogu värbamisprotsessi jooksul ning saadaks teatisi värbamistöörühmale ja kandidaadile.</span><span class="sxs-lookup"><span data-stu-id="07407-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="07407-141">Üldiselt saab lahenduses Common Data Service salvestatud üksuste jaoks voogusid seadistada nii, et need saadavad teatisi rakenduse Core HR, Attract või Dynamics 365 Talent: Onboard sündmuste kohta.</span><span class="sxs-lookup"><span data-stu-id="07407-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="07407-142">Malli **Flow – meiliteatis** alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Flow – meiliteatis](https://go.microsoft.com/fwlink/?linkid=2082103).</span><span class="sxs-lookup"><span data-stu-id="07407-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="07407-143">Flow – SQL-i ühendamine ja käivitamine</span><span class="sxs-lookup"><span data-stu-id="07407-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="07407-144">Mall **Flow – SQL-i ühendamine ja käivitamine** loob ühenduse Microsoft SQL Serveriga ja lubab käivitada SQL-i päringuid.</span><span class="sxs-lookup"><span data-stu-id="07407-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="07407-145">Kuigi see mall on mõeldud lugema ja värskendama SQL-i tabeleid, saab seda laiendada kasutamiseks teistes stsenaariumites.</span><span class="sxs-lookup"><span data-stu-id="07407-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="07407-146">Näiteks saab seda kasutada vahetabeli täitmiseks teenuses Common Data Service kirjetega SQL Serverist ja vahetabeli aeg-ajalt sünkroonimiseks, kasutades SQL Serveri astmelist jaotust.</span><span class="sxs-lookup"><span data-stu-id="07407-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="07407-147">Malli **Flow – SQL-i ühendamine ja käivitamine** alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Flow – SQL-i ühendamine ja käivitamine](https://go.microsoft.com/fwlink/?linkid=2081789).</span><span class="sxs-lookup"><span data-stu-id="07407-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="07407-148">Flow – SharePointi integreerimine</span><span class="sxs-lookup"><span data-stu-id="07407-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="07407-149">Malli **Flow – SharePointi integreerimine** saab kasutada andmete lugemiseks Microsoft SharePointi loendist, loendi võrdlemiseks teenuse Common Data Service mis tahes üksuse väljaväärtustega ja võrdluse tulemuste saatmiseks teavitusmeilina.</span><span class="sxs-lookup"><span data-stu-id="07407-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="07407-150">Organisatsioonil võivad olla oskused, mida tal on tingimata vaja.</span><span class="sxs-lookup"><span data-stu-id="07407-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="07407-151">Neid oskusi saab hoiustada SharePointis SharePointi loendina.</span><span class="sxs-lookup"><span data-stu-id="07407-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="07407-152">Kui kandidaat kandideerib mis tahes tööle, mille kohta on olemas vajalike oskuste loend, ning kandidaadi oskuse ja SharePointi salvestatud oskuste vahel on oluline kokkulangevus, saadetakse selle kohta teavitusmeil.</span><span class="sxs-lookup"><span data-stu-id="07407-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="07407-153">Nii täidetakse kiiresti vajaminevad ametikohad kiiremini, kuna teatised aitavad värbajatel jõuda kõigi organisatsiooni kandidaatideni ja neid värvata.</span><span class="sxs-lookup"><span data-stu-id="07407-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="07407-154">Seda malli saab laiendada kasutamiseks mis tahes stsenaariumi jaoks, mis hõlmab SharePointi integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="07407-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="07407-155">Malli **Flow – SharePointi integratsioon** alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Flow – SharePointi integratsioon](https://go.microsoft.com/fwlink/?linkid=2082109).</span><span class="sxs-lookup"><span data-stu-id="07407-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>



## <a name="additional-resources"></a><span data-ttu-id="07407-156">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="07407-156">Additional resources</span></span>

[<span data-ttu-id="07407-157">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="07407-157">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="07407-158">Rakenduse ülekandmine rentnike ja keskkondade vahel</span><span class="sxs-lookup"><span data-stu-id="07407-158">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
