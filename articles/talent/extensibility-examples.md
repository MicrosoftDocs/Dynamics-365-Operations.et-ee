---
title: Talenti laiendamine Power Appsi ja Power Automate’iga
description: Selles artiklis kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 Talent - Attract, mis kasutab Microsoft Power Appsi ja Microsoft Power Automate’i.
author: negudava
manager: Annbe
ms.date: 02/06/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1051fa4db16bb94cc9d60a91fc3637d7e5305cc2
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029907"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="4a58e-103">Talenti laiendamine Power Appsi ja Power Automate’iga</span><span class="sxs-lookup"><span data-stu-id="4a58e-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="4a58e-104">Selles artiklis kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 Talent: Attract, mis kasutab Microsoft Power Appsi ja Microsoft Power Automate’i.</span><span class="sxs-lookup"><span data-stu-id="4a58e-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="4a58e-105">Saate rakenduse Power Apps keskkonda importida iga näitega seotud lahendusepaketi.</span><span class="sxs-lookup"><span data-stu-id="4a58e-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="4a58e-106">Seejärel saate pakette kasutada juhisena või lähtekohana teie organisatsioonile sobivate stsenaariumide rakendamiseks.</span><span class="sxs-lookup"><span data-stu-id="4a58e-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a58e-107">Kui soovite kasutada selles teemas kirjeldatud malle ja rakendust muutmata kujul, katsetage neid kindlasti veendumaks, et need hõlmavad kõiki teie juurutusele kehtivaid stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="4a58e-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="4a58e-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="4a58e-108">Prerequisites</span></span>

- <span data-ttu-id="4a58e-109">Pakettide importimiseks peab kasutajatel olema **keskkonna looja** luba.</span><span class="sxs-lookup"><span data-stu-id="4a58e-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="4a58e-110">Rakenduste eksportimiseks või importimiseks peab kasutajatel olema Power Appsi plaani 2 litsents või Power Appsi plaani 2 proovilitsents.</span><span class="sxs-lookup"><span data-stu-id="4a58e-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="4a58e-111">Power Automate’i ja Formi ühendamine</span><span class="sxs-lookup"><span data-stu-id="4a58e-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="4a58e-112">Malli **Power Automate’i ja Formi ühendamine** saab kasutada andmete lugemiseks Microsoft Formsist ja nende salvestamiseks teenuse Common Data Service üksusesse.</span><span class="sxs-lookup"><span data-stu-id="4a58e-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="4a58e-113">Seda malli saab laiendada, et seda saaks kasutada ka teistes stsenaariumites.</span><span class="sxs-lookup"><span data-stu-id="4a58e-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="4a58e-114">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="4a58e-114">Here are some examples:</span></span>

- <span data-ttu-id="4a58e-115">Kandidaadi hinnangute jäädvustamine.</span><span class="sxs-lookup"><span data-stu-id="4a58e-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="4a58e-116">Kursuse küsimustike tulemuste jäädvustamine.</span><span class="sxs-lookup"><span data-stu-id="4a58e-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="4a58e-117">Töövestluse küsimuste teegi koostamine inimressursside (HR) administraatorite jaoks.</span><span class="sxs-lookup"><span data-stu-id="4a58e-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="4a58e-118">Kandidaadi hinnangu jäädvustamine vestluse protsessi kohta</span><span class="sxs-lookup"><span data-stu-id="4a58e-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="4a58e-119">Microsoft Dynamics 365: Attractis saab vorme kasutada kandidaadi portaalis, kus kandidaadid täidavad üksikasju.</span><span class="sxs-lookup"><span data-stu-id="4a58e-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="4a58e-120">Vorme saate ka tegevustena töömalli manustada.</span><span class="sxs-lookup"><span data-stu-id="4a58e-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="4a58e-121">Kui kandidaat vormi esitab, jäädvustab Microsoft Power Automate vormi esitamise, loeb andmeid ja salvestab need teenuse Common Data Service üksusesse.</span><span class="sxs-lookup"><span data-stu-id="4a58e-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="4a58e-122">Malli **Power Automate’i ja Formi ühendamine** ja kohandatud üksuse struktuuri alla laadimiseks avage Microsofti allalaadimiskeskuses [Power Automate’i ja Formi ühendamine](https://go.microsoft.com/fwlink/?linkid=2081988).</span><span class="sxs-lookup"><span data-stu-id="4a58e-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="4a58e-123">Power Automate – SharePointiga integreerimine</span><span class="sxs-lookup"><span data-stu-id="4a58e-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="4a58e-124">Malli **Power Automate – SharePointiga integreerimine** saab kasutada andmete lugemiseks Microsoft SharePointi loendist, loendi võrdlemiseks olemi Common Data Service mis tahes üksuse väljaväärtustega ja võrdluse tulemuste saatmiseks teavitusmeilina.</span><span class="sxs-lookup"><span data-stu-id="4a58e-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="4a58e-125">Organisatsioonil võivad olla oskused, mida tal on tingimata vaja.</span><span class="sxs-lookup"><span data-stu-id="4a58e-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="4a58e-126">Neid oskusi saab hoiustada SharePointis SharePointi loendina.</span><span class="sxs-lookup"><span data-stu-id="4a58e-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="4a58e-127">Kui kandidaat kandideerib mis tahes tööle, mille kohta on olemas vajalike oskuste loend, ning kandidaadi oskuse ja SharePointi salvestatud oskuste vahel on oluline kokkulangevus, saadetakse selle kohta teavitusmeil.</span><span class="sxs-lookup"><span data-stu-id="4a58e-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="4a58e-128">See aitab täita vajaminevad ametikohad kiiremini, kuna teatised aitavad värbajatel värvata kandidaate kogu organisatsioonist.</span><span class="sxs-lookup"><span data-stu-id="4a58e-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="4a58e-129">Seda malli saab laiendada kasutamiseks mis tahes stsenaariumi jaoks, mis hõlmab SharePointi integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="4a58e-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="4a58e-130">Malli **Power Automate – SharePointiga integreerimine** allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Automate – SharePointiga integreerimine](https://go.microsoft.com/fwlink/?linkid=2082109).</span><span class="sxs-lookup"><span data-stu-id="4a58e-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="4a58e-131">Soovitusrakendus</span><span class="sxs-lookup"><span data-stu-id="4a58e-131">Referral App</span></span>

<span data-ttu-id="4a58e-132">Saate kasutada soovitusrakendust, et lisada kandidaate jagatud talendipanka.</span><span class="sxs-lookup"><span data-stu-id="4a58e-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="4a58e-133">Soovitaja saab kandidaadi esitamisel sisestada **eesnime**, **perekonnanime**, **meiliaadressi** ja **LinkedIni URLi**.</span><span class="sxs-lookup"><span data-stu-id="4a58e-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="4a58e-134">Seejärel täidetakse kandidaatallika metaandmed koos soovitaja teabega.</span><span class="sxs-lookup"><span data-stu-id="4a58e-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="4a58e-135">Saate selle rakenduse manustada soovituste esitamiseks töötajate iseteenindusse või kasutada seda ettevõtteportaalis hüperlingina ja kasutada eraldiseisva rakendusena.</span><span class="sxs-lookup"><span data-stu-id="4a58e-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="4a58e-136">**Sooitusrakenduse** allalaadimiseks minge Microsofti allalaadimiskeskuse lehele [Dynamics 365 Talent laiendatavuse lahendus: soovitusrakendus](https://www.microsoft.com/download/details.aspx?id=58497).</span><span class="sxs-lookup"><span data-stu-id="4a58e-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="4a58e-137">Seda rakendust saab importida ja kohandada, et lisada täiendavaid funktsioone.</span><span class="sxs-lookup"><span data-stu-id="4a58e-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a58e-138">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4a58e-138">Additional resources</span></span>

[<span data-ttu-id="4a58e-139">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="4a58e-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="4a58e-140">Rakenduse ülekandmine rentnike ja keskkondade vahel</span><span class="sxs-lookup"><span data-stu-id="4a58e-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
