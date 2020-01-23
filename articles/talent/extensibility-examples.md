---
title: Talenti laiendamine Power Appsi ja Power Automate’iga
description: Selles teemas kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 Talent, mis kasutab Microsoft Power Appsi ja Microsoft Power Automate’i.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
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
ms.openlocfilehash: 6c8a583a93c2ceb70d8c3b0e0047e2bf2047b56d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898313"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="3a321-103">Talenti laiendamine Power Appsi ja Power Automate’iga</span><span class="sxs-lookup"><span data-stu-id="3a321-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="3a321-104">Selles teemas kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 Talent, mis kasutab Microsoft Power Appsi ja Microsoft Power Automate’i.</span><span class="sxs-lookup"><span data-stu-id="3a321-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="3a321-105">Saate rakenduse Power Apps keskkonda importida iga näitega seotud lahendusepaketi.</span><span class="sxs-lookup"><span data-stu-id="3a321-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="3a321-106">Seejärel saate pakette kasutada juhisena või lähtekohana teie organisatsioonile sobivate stsenaariumide rakendamiseks.</span><span class="sxs-lookup"><span data-stu-id="3a321-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a321-107">Kui soovite kasutada selles teemas kirjeldatud malle ja rakendust muutmata kujul, katsetage neid kindlasti veendumaks, et need hõlmavad kõiki teie juurutusele kehtivaid stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="3a321-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="3a321-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="3a321-108">Prerequisites</span></span>

- <span data-ttu-id="3a321-109">Pakettide importimiseks peab kasutajatel olema **keskkonna looja** luba.</span><span class="sxs-lookup"><span data-stu-id="3a321-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="3a321-110">Rakenduste eksportimiseks või importimiseks peab kasutajatel olema Power Appsi plaani 2 litsents või Power Appsi plaani 2 proovilitsents.</span><span class="sxs-lookup"><span data-stu-id="3a321-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="3a321-111">Power Automate’i ja Formi ühendamine</span><span class="sxs-lookup"><span data-stu-id="3a321-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="3a321-112">Malli **Power Automate’i ja Formi ühendamine** saab kasutada andmete lugemiseks Microsoft Formsist ja nende salvestamiseks teenuse Common Data Service üksusesse.</span><span class="sxs-lookup"><span data-stu-id="3a321-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="3a321-113">Seda malli saab laiendada, et seda saaks kasutada ka teistes stsenaariumites.</span><span class="sxs-lookup"><span data-stu-id="3a321-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="3a321-114">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="3a321-114">Here are some examples:</span></span>

- <span data-ttu-id="3a321-115">Kandidaadi hinnangute jäädvustamine.</span><span class="sxs-lookup"><span data-stu-id="3a321-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="3a321-116">Kursuse küsimustike tulemuste jäädvustamine.</span><span class="sxs-lookup"><span data-stu-id="3a321-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="3a321-117">Töövestluse küsimuste teegi koostamine inimressursside (HR) administraatorite jaoks.</span><span class="sxs-lookup"><span data-stu-id="3a321-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="3a321-118">Kandidaadi hinnangu jäädvustamine vestluse protsessi kohta</span><span class="sxs-lookup"><span data-stu-id="3a321-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="3a321-119">Microsoft Dynamics 365: Attractis saab vorme kuvada kandidaadi portaalis ja kandidaadid saavad täita üksikasju.</span><span class="sxs-lookup"><span data-stu-id="3a321-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="3a321-120">Vorme saab ka tegevustena töömalli manustada.</span><span class="sxs-lookup"><span data-stu-id="3a321-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="3a321-121">Kui kandidaat vormi esitab, jäädvustab Microsoft Power Automate vormi esitamise, loeb andmeid ja salvestab need teenuse Common Data Service üksusesse.</span><span class="sxs-lookup"><span data-stu-id="3a321-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="3a321-122">Malli **Power Automate’i ja Formi ühendamine** ja kohandatud üksuse struktuuri alla laadimiseks avage Microsofti allalaadimiskeskuses [Power Automate’i ja Formi ühendamine](https://go.microsoft.com/fwlink/?linkid=2081988).</span><span class="sxs-lookup"><span data-stu-id="3a321-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a><span data-ttu-id="3a321-123">Power Appsi edastatud parameetrite käivitamine ja ekstraktimine</span><span class="sxs-lookup"><span data-stu-id="3a321-123">Initiate and Extract Parameters Passed to Power Apps</span></span>

<span data-ttu-id="3a321-124">Malli **Power Appsi edastatud parameetrite käivitamine ja ekstraktimine** saab kasutada lähtekohana mis tahes rakenduse Power Apps stsenaariumi jaoks, mis on omane Attractile.</span><span class="sxs-lookup"><span data-stu-id="3a321-124">The **Initiate and Extract Parameters Passed to Power Apps** template can be used as a starting point for any Power Apps scenario that is specific to Attract.</span></span> <span data-ttu-id="3a321-125">See sisaldab kõiki vaikeparameetreid, mille Attract edastab, nt **Tööavaldus**, **Kandidaadi ID** ja **Töö ID**.</span><span class="sxs-lookup"><span data-stu-id="3a321-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="3a321-126">Seda malli saab kasutada kandidaadi hinnanguvormi leidmiseks, et personalijuht saaks kandidaadi täidetud hinnangut vaadata.</span><span class="sxs-lookup"><span data-stu-id="3a321-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="3a321-127">Power Appsiga loodud rakendusi saab manustada Attractis töömalli.</span><span class="sxs-lookup"><span data-stu-id="3a321-127">Apps that are created by using Power Apps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="3a321-128">Malli **Power Appsi edastatud parameetrite käivitamine ja ekstraktimine** ja kohandatud üksuse struktuuri allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Appsi edastatud parameetrite käivitamine ja ekstraktimine](https://go.microsoft.com/fwlink/?linkid=2081991).</span><span class="sxs-lookup"><span data-stu-id="3a321-128">To download the **Initiate and Extract Parameters Passed to Power Apps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="3a321-129">Office 365-iga integreerimine</span><span class="sxs-lookup"><span data-stu-id="3a321-129">Integration with Office 365</span></span>

<span data-ttu-id="3a321-130">Rakendust **Office 365-ga integreerimine** saab kasutada sisse logitud kasutajate töörühma teabe ekstraktimiseks Microsoft Office 365-st.</span><span class="sxs-lookup"><span data-stu-id="3a321-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="3a321-131">See viitab töötajatele Talentis, et ekstraktida sisse- ja väljaregistreerimiste üksikasju ning erandite kirjeid.</span><span class="sxs-lookup"><span data-stu-id="3a321-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="3a321-132">Sisse- ja väljaregistreerimiste üksikasju salvestatakse teenuse Common Data Service kohandatud üksustes.</span><span class="sxs-lookup"><span data-stu-id="3a321-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="3a321-133">Eeldus on, et need üksikasjad täidab muude tootjate süsteemid integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="3a321-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="3a321-134">Seda rakendust saab laiendada, et seda saaks kasutada ka teistes stsenaariumites.</span><span class="sxs-lookup"><span data-stu-id="3a321-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="3a321-135">Näiteks saab seda kasutada töörühma puhkuste teabe, kalendrisündmuste ja töörühmaga seotud sündmuste näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="3a321-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="3a321-136">Rakenduse **Office 365-ga integreerimine** ja kohandatud üksuse struktuuri alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Office 365-ga integreerimine](https://go.microsoft.com/fwlink/?linkid=2081787).</span><span class="sxs-lookup"><span data-stu-id="3a321-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--email-notification"></a><span data-ttu-id="3a321-137">Power Automate – meiliteatis</span><span class="sxs-lookup"><span data-stu-id="3a321-137">Power Automate – Email Notification</span></span>

<span data-ttu-id="3a321-138">Malli **Power Automate – meiliteatis** saab kasutada meiliteatise stsenaariumide jaoks.</span><span class="sxs-lookup"><span data-stu-id="3a321-138">The **Power Automate – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="3a321-139">Seda saab kasutada teavitusmeilide saatmiseks kandidaatidele, kelle värbamistöörühm värbamisprotsessi mis tahes etapis tagasi lükkab.</span><span class="sxs-lookup"><span data-stu-id="3a321-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="3a321-140">Seda malli saab laiendada, et see jälgiks muudatusi kandidaadi etapis kogu värbamisprotsessi jooksul ning saadaks teatisi värbamistöörühmale ja kandidaadile.</span><span class="sxs-lookup"><span data-stu-id="3a321-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="3a321-141">Üldiselt saab lahenduses Common Data Service salvestatud üksuste jaoks voogusid seadistada nii, et need saadavad teatisi rakenduse Core HR, Attract või Onboard sündmuste kohta.</span><span class="sxs-lookup"><span data-stu-id="3a321-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Onboard.</span></span>

<span data-ttu-id="3a321-142">Malli **Power Automate – meiliteatis** allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Automate – meiliteatis](https://go.microsoft.com/fwlink/?linkid=2082103).</span><span class="sxs-lookup"><span data-stu-id="3a321-142">To download the **Power Automate – Email Notification** template, go to [Power Automate – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="3a321-143">Power Automate – SQL-i ühendamine ja käivitamine</span><span class="sxs-lookup"><span data-stu-id="3a321-143">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="3a321-144">Mall **Power Automate – SQL-i ühendamine ja käivitamine** loob ühenduse Microsoft SQL Serveriga ja lubab käivitada SQL-i päringuid.</span><span class="sxs-lookup"><span data-stu-id="3a321-144">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="3a321-145">Kuigi see mall on mõeldud lugema ja värskendama SQL-i tabeleid, saab seda laiendada kasutamiseks teistes stsenaariumites.</span><span class="sxs-lookup"><span data-stu-id="3a321-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="3a321-146">Näiteks saab seda kasutada vahetabeli täitmiseks teenuses Common Data Service kirjetega SQL Serverist ja vahetabeli aeg-ajalt sünkroonimiseks, kasutades SQL Serveri astmelist jaotust.</span><span class="sxs-lookup"><span data-stu-id="3a321-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="3a321-147">Malli **Power Automate – SQL-i ühendamine ja käivitamine** allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Automate – SQL-i ühendamine ja käivitamine](https://go.microsoft.com/fwlink/?linkid=2081789).</span><span class="sxs-lookup"><span data-stu-id="3a321-147">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="3a321-148">Power Automate – SharePointiga integreerimine</span><span class="sxs-lookup"><span data-stu-id="3a321-148">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="3a321-149">Malli **Power Automate – SharePointiga integreerimine** saab kasutada andmete lugemiseks Microsoft SharePointi loendist, loendi võrdlemiseks olemi Common Data Service mis tahes üksuse väljaväärtustega ja võrdluse tulemuste saatmiseks teavitusmeilina.</span><span class="sxs-lookup"><span data-stu-id="3a321-149">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="3a321-150">Organisatsioonil võivad olla oskused, mida tal on tingimata vaja.</span><span class="sxs-lookup"><span data-stu-id="3a321-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="3a321-151">Neid oskusi saab hoiustada SharePointis SharePointi loendina.</span><span class="sxs-lookup"><span data-stu-id="3a321-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="3a321-152">Kui kandidaat kandideerib mis tahes tööle, mille kohta on olemas vajalike oskuste loend, ning kandidaadi oskuse ja SharePointi salvestatud oskuste vahel on oluline kokkulangevus, saadetakse selle kohta teavitusmeil.</span><span class="sxs-lookup"><span data-stu-id="3a321-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="3a321-153">Nii täidetakse kiiresti vajaminevad ametikohad kiiremini, kuna teatised aitavad värbajatel jõuda kõigi organisatsiooni kandidaatideni ja neid värvata.</span><span class="sxs-lookup"><span data-stu-id="3a321-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="3a321-154">Seda malli saab laiendada kasutamiseks mis tahes stsenaariumi jaoks, mis hõlmab SharePointi integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="3a321-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="3a321-155">Malli **Power Automate – SharePointiga integreerimine** allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Automate – SharePointiga integreerimine](https://go.microsoft.com/fwlink/?linkid=2082109).</span><span class="sxs-lookup"><span data-stu-id="3a321-155">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="3a321-156">Soovitusrakendus</span><span class="sxs-lookup"><span data-stu-id="3a321-156">Referral App</span></span>
<span data-ttu-id="3a321-157">Saate kasutada soovitusrakendust, et lisada kandidaate jagatud talendipanka.</span><span class="sxs-lookup"><span data-stu-id="3a321-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="3a321-158">Soovitaja saab kandidaadi esitamisel sisestada **eesnime**, **perekonnanime**, **meliaadressi** ja **LinkedIni URLi**.</span><span class="sxs-lookup"><span data-stu-id="3a321-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="3a321-159">Seejärel täidetakse kandidaatallika metaandmed koos soovitaja teabega.</span><span class="sxs-lookup"><span data-stu-id="3a321-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="3a321-160">Saate selle rakenduse manustada soovituste esitamiseks töötajate iseteenindusse (ESS) või kasutada seda ettevõtteportaalis hüperlingina ja kasutada eraldiseisva rakendusena.</span><span class="sxs-lookup"><span data-stu-id="3a321-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="3a321-161">**Sooitusrakenduse** allalaadimiseks minge Microsofti allalaadimiskeskuse lehele [Dynamics 365 Talent laiendatavuse lahendus: soovitusrakendus](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d).</span><span class="sxs-lookup"><span data-stu-id="3a321-161">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="3a321-162">Seda rakendust saab importida ja kohandada, et lisada täiendavaid funktsioone.</span><span class="sxs-lookup"><span data-stu-id="3a321-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a321-163">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3a321-163">Additional resources</span></span>

[<span data-ttu-id="3a321-164">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="3a321-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="3a321-165">Rakenduse ülekandmine rentnike ja keskkondade vahel</span><span class="sxs-lookup"><span data-stu-id="3a321-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
