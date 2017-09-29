---
title: "Pilvjuurutuste süsteeminõuded"
description: "Teema esitab süsteeminõuete loendi rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition pilvejuurutuste kohta."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 5230911e1febc66b294f1331846373a472789adf
ms.openlocfilehash: 46eacb2a01c3bfcc7144c7d8c39ee0189fd72e16
ms.contentlocale: et-ee
ms.lasthandoff: 08/04/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="69e07-103">Pilvjuurutuste süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="69e07-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="69e07-104">Teema esitab süsteeminõuete loendi rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition pilvejuurutuste kohta.</span><span class="sxs-lookup"><span data-stu-id="69e07-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="69e07-105">Enne rakenduse Finance and Operations installimist kontrollige vajaduse korral, kas süsteem, millega töötate, vastab minimaalsetele võrgu-, riistvara- või tarkvaranõuetele või ületab neid.</span><span class="sxs-lookup"><span data-stu-id="69e07-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="69e07-106">Toetatud veebibrauserid</span><span class="sxs-lookup"><span data-stu-id="69e07-106">Supported web browsers</span></span>
<span data-ttu-id="69e07-107">Veebirakenduse võib töötada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemis.</span><span class="sxs-lookup"><span data-stu-id="69e07-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="69e07-108">Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s</span><span class="sxs-lookup"><span data-stu-id="69e07-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="69e07-109">Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7</span><span class="sxs-lookup"><span data-stu-id="69e07-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="69e07-110">Google Chrome (viimane avalikult saadaolev versioon) operatsioonisüsteemides Windows 10, Windows 8.1, Windows 8, Windows 7 või tahvelarvuti Google Nexus 10</span><span class="sxs-lookup"><span data-stu-id="69e07-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="69e07-111">Apple Safari (viimane avalikult väljastatud versioon) operatsioonisüsteemides Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) või 10.12 (Sierra) või Apple iPad</span><span class="sxs-lookup"><span data-stu-id="69e07-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="69e07-112">Iga veebibrauseri uusima versiooni leidmiseks minge tarkvaratootja veebisaidile.</span><span class="sxs-lookup"><span data-stu-id="69e07-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="69e07-113">Peate installima väljalaske-eelse Chrome’i versiooni, et lubada kuvatõmmise piltide salvestamine tegevuse salvestajas ja nende lisamine loodud Microsoft Wordi dokumentidesse.</span><span class="sxs-lookup"><span data-stu-id="69e07-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="69e07-114">Töövooredaktor käivitatakse ClickOnce’i rakendusena.</span><span class="sxs-lookup"><span data-stu-id="69e07-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="69e07-115">Ainult Microsoft Edge ja Internet Explorer (Microsoft Windowsi toetatud versioonis) toetavad ClickOnce’i rakendusi.</span><span class="sxs-lookup"><span data-stu-id="69e07-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="69e07-116">Töövooredaktori ClickOnce rakendus nõuab ühilduvat 64-bitist operatsioonisüsteemi.</span><span class="sxs-lookup"><span data-stu-id="69e07-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="69e07-117">Finantsaruandluse jaoks mõeldud aruandekujundaja käivitatakse ClickOnce’i rakendusena.</span><span class="sxs-lookup"><span data-stu-id="69e07-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="69e07-118">See nõuab ühilduvat 64-bitist operatsioonisüsteemi.</span><span class="sxs-lookup"><span data-stu-id="69e07-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="69e07-119">Kui kasutate Chrome’i, peate aruandekoosturi kliendi allalaadimiseks installima laienduse ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="69e07-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="69e07-120">Kui kasutate Chrome’i inkognito-režiimis, siis veenduge, et laiendus ClickOnce oleks inkognito-režiimi jaoks samuti aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="69e07-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="69e07-121">PDF-failide eelvaateks soovitame kasutada brausereid, nagu Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s või Google Chrome (viimane avalikult saadaolev versioon) Windows 10-s, Windows 8.1-s, Windows 8-s, Windows 7-s või tahvelarvutis Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="69e07-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="69e07-122">Retail Cloud POS-i toetatud veebibrauserid</span><span class="sxs-lookup"><span data-stu-id="69e07-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="69e07-123">Retail Cloud POS võib töötada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemides.</span><span class="sxs-lookup"><span data-stu-id="69e07-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="69e07-124">Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s</span><span class="sxs-lookup"><span data-stu-id="69e07-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="69e07-125">Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7</span><span class="sxs-lookup"><span data-stu-id="69e07-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="69e07-126">Chrome (kõige värskem saadaolev versioon) operatsioonisüsteemis Windows 10, Windows 8.1 või Windows 7</span><span class="sxs-lookup"><span data-stu-id="69e07-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="69e07-127">Võrgunõuded</span><span class="sxs-lookup"><span data-stu-id="69e07-127">Network requirements</span></span>
-   <span data-ttu-id="69e07-128">Finance and Operations on mõeldud võrkudele, mille latentsus on kuni 250–300 millisekundit (ms).</span><span class="sxs-lookup"><span data-stu-id="69e07-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="69e07-129">See on latentsus brauserikliendist Microsoft Azure’i andmekeskusesse, mis majutab rakendust Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="69e07-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="69e07-130">Soovitame teilt testida võrgulatentsust veebiaadressil <http://www.azurespeed.com>.</span><span class="sxs-lookup"><span data-stu-id="69e07-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="69e07-131">Rakenduse Finance and Operations ribalaiuse nõuded sõltuvad stsenaariumist.</span><span class="sxs-lookup"><span data-stu-id="69e07-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="69e07-132">Kõige tüüpilisemad stsenaariumid nõuavad ribalaiust rohkem kui 50 kilobaiti sekundis (KB/s).</span><span class="sxs-lookup"><span data-stu-id="69e07-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="69e07-133">Stsenaariumide puhul, millel on kõrged kasuliku koormuse nõuded (nt tööruumid või stsenaariumid, mis hõlmavad ulatuslikku kohandamist), on soovitatav kasutada rohkem ribalaiust.</span><span class="sxs-lookup"><span data-stu-id="69e07-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="69e07-134">Üldiselt on Finance and Operations Interneti jaoks optimeeritud.</span><span class="sxs-lookup"><span data-stu-id="69e07-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="69e07-135">Pendellevi hulk brauserikliendist Azure’i andmekeskusesse on väga väike ja kogu kasulik koormus on tihendatud.</span><span class="sxs-lookup"><span data-stu-id="69e07-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="69e07-136">Ärge arvutage ribalaiuse nõudeid kliendi asukohast, korrutades kasutajate arvu minimaalsete ribalaiuse nõuetega.</span><span class="sxs-lookup"><span data-stu-id="69e07-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="69e07-137">Antud asukoha samaaegset kasutust on väga keeruline arvutada.</span><span class="sxs-lookup"><span data-stu-id="69e07-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="69e07-138">Ribalaiuse nõuete pärast muret tundvate klientide puhul kasutage rakenduse Finance and Operations eelvaateversiooni.</span><span class="sxs-lookup"><span data-stu-id="69e07-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="69e07-139">.NET Frameworki nõuded</span><span class="sxs-lookup"><span data-stu-id="69e07-139">.NET Framework requirements</span></span>
<span data-ttu-id="69e07-140">Finance and Operations nõuab Microsoft .NET Frameworki versiooni 4.6.2 kõikide ClickOnce-tüüpi rakenduste puhul (nt dokumendi marsruudivaliku agent).</span><span class="sxs-lookup"><span data-stu-id="69e07-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="69e07-141">Installimisjuhiste puhul vaadake teemat [.NET Frameworki installimine](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="69e07-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="69e07-142">Toetatud Microsoft Office’i rakendused</span><span class="sxs-lookup"><span data-stu-id="69e07-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="69e07-143">Rakenduse Finance and Operations pilve- ja kohapealsetes juurutustes toetatakse järgmisi Microsoft Office’i rakendusi.</span><span class="sxs-lookup"><span data-stu-id="69e07-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="69e07-144">Microsoft Exceli ja Wordi lisandmooduli käivitamiseks peab teil olema installitud Windowsile või Macile mõeldud Microsoft Office 2016.</span><span class="sxs-lookup"><span data-stu-id="69e07-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="69e07-145">Versiooninõuete kohta lisateabe saamiseks vaadake teemat [Office’i integratsiooni tõrkeotsing](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="69e07-145">For more information about version requirements, see [Office integration troubleshooting](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).</span></span>
-   <span data-ttu-id="69e07-146">Funktsiooniga Ekspordi Excelisse või Ekspordi Wordi loodud dokumentide vaatamiseks peab teil olema installitud Microsoft Office 2007 või uuem versioon.</span><span class="sxs-lookup"><span data-stu-id="69e07-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="69e07-147">Retail Modern POS-i nõuded</span><span class="sxs-lookup"><span data-stu-id="69e07-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="69e07-148">Kui Retail Modern POS kasutab võrguühenduseta andmebaasi, peab arvuti vastama kõikidele Microsoft SQL Serveri nõuetele.</span><span class="sxs-lookup"><span data-stu-id="69e07-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="69e07-149">Retail Modern POS-i võrguühenduseta andmebaas töötab teenusega Microsoft SQL Server 2012, millel on hoolduspakett Service Pack 3 või uuem, teenusega Microsoft SQL Server 2014, millel on hoolduspakett Service Pack 2 või uuem, ja teenusega teenusega Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="69e07-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="69e07-150">Soovitame alati kasutada uusimat saadaolevat väljannet ja installida uusimad hoolduspaketid.</span><span class="sxs-lookup"><span data-stu-id="69e07-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="69e07-151">Toetatud operatsioonisüsteemid</span><span class="sxs-lookup"><span data-stu-id="69e07-151">Supported operating systems</span></span>

-   <span data-ttu-id="69e07-152">Retail Modern POS on 32-bitine rakendus, kuid see võib töötada nii x86- kui ka x64-põhistes arhitektuurides.</span><span class="sxs-lookup"><span data-stu-id="69e07-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="69e07-153">Retail Modern POS on toetatud ainult operatsioonisüsteemi Windows 10 Pro, Enterprise ja Enterprise Long Term Servicing Branch (LTSB) versioonides.</span><span class="sxs-lookup"><span data-stu-id="69e07-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="69e07-154">Minimaalsed süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="69e07-154">Minimum system requirements</span></span>

-   <span data-ttu-id="69e07-155">Minimaalne toetatud eraldusvõime on 1280 × 1024.</span><span class="sxs-lookup"><span data-stu-id="69e07-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="69e07-156">Retail Modern POS-i käitav arvuti peab vastama nendele nõuetele.</span><span class="sxs-lookup"><span data-stu-id="69e07-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="69e07-157">Sellel peab olema minimaalselt kahetuumaline protsessor, mis töötab vähem kui 2 gigahertsiga (GHz).</span><span class="sxs-lookup"><span data-stu-id="69e07-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="69e07-158">Sellel peab olema minimaalselt 3 gigabaiti (GB) RAM-i.</span><span class="sxs-lookup"><span data-stu-id="69e07-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="69e07-159">Sellel peab olema Interneti-juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="69e07-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="69e07-160">Jaemüügi riistvarajaama nõuded</span><span class="sxs-lookup"><span data-stu-id="69e07-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="69e07-161">Toetatud operatsioonisüsteemid</span><span class="sxs-lookup"><span data-stu-id="69e07-161">Supported operating systems</span></span>

-   <span data-ttu-id="69e07-162">Jaemüügi riistvarajaam on 32-bitine rakendus, kuid see võib töötada nii x86- kui ka 64-põhistes arhitektuurides.</span><span class="sxs-lookup"><span data-stu-id="69e07-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="69e07-163">Jaemüügi riistvarajaama toetatakse järgmistes operatsioonisüsteemides:</span><span class="sxs-lookup"><span data-stu-id="69e07-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="69e07-164">Windows 7 Professionali, Enterprise’i ja Ultimate’i versioonides</span><span class="sxs-lookup"><span data-stu-id="69e07-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="69e07-165">Windows 7 toetatakse ainult siis, kui Internet Explorer 11 on käsitsi arvutisse installitud.</span><span class="sxs-lookup"><span data-stu-id="69e07-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="69e07-166">Windows 8.1 Update 1 Professionali, Enterprise’i ja manustatud versioonid</span><span class="sxs-lookup"><span data-stu-id="69e07-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="69e07-167">Windows 10 Pro, Enterprise’i ja Enterprise LTSB versioonid</span><span class="sxs-lookup"><span data-stu-id="69e07-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="69e07-168">Minimaalsed süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="69e07-168">Minimum system requirements</span></span>

<span data-ttu-id="69e07-169">Arvuti peab vastama kõigile järgmiste üksuste installimist ja kasutamist puudutavatele süsteeminõuetele.</span><span class="sxs-lookup"><span data-stu-id="69e07-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="69e07-170">Interneti teabeteenuste haldamine (IIS)</span><span class="sxs-lookup"><span data-stu-id="69e07-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="69e07-171">Muu osapoole riistvara</span><span class="sxs-lookup"><span data-stu-id="69e07-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="69e07-172">Jaekaupluse skaala üksuse nõuded</span><span class="sxs-lookup"><span data-stu-id="69e07-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="69e07-173">Toetatud operatsioonisüsteemid</span><span class="sxs-lookup"><span data-stu-id="69e07-173">Supported operating systems</span></span>

-   <span data-ttu-id="69e07-174">Jaekaupluse skaala üksus on 32-bitine rakendus, kuid see võib töötada nii x86- kui ka 64-põhistes arhitektuurides.</span><span class="sxs-lookup"><span data-stu-id="69e07-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="69e07-175">Jaekaupluse skaala üksust toetatakse järgmistes operatsioonisüsteemides:</span><span class="sxs-lookup"><span data-stu-id="69e07-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="69e07-176">Windows 7 Professionali, Enterprise’i ja Ultimate’i versioonides</span><span class="sxs-lookup"><span data-stu-id="69e07-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="69e07-177">Windows 8.1 Update 1 Professionali, Enterprise’i ja manustatud versioonid</span><span class="sxs-lookup"><span data-stu-id="69e07-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="69e07-178">Windows 10 Pro, Enterprise’i ja Enterprise LTSB versioonid</span><span class="sxs-lookup"><span data-stu-id="69e07-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="69e07-179">Minimaalsed süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="69e07-179">Minimum system requirements</span></span>

-   <span data-ttu-id="69e07-180">4 GB RAM-i</span><span class="sxs-lookup"><span data-stu-id="69e07-180">4 GB of RAM</span></span>
-   <span data-ttu-id="69e07-181">1,6 GHz CPU tippkiirus tuuma kohta (kaks tuuma minimaalselt.)</span><span class="sxs-lookup"><span data-stu-id="69e07-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="69e07-182">Vähemalt 10 GB vaba ruumi (kanali andmebaas võib nõuda suurel hulgal ruumi)</span><span class="sxs-lookup"><span data-stu-id="69e07-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="69e07-183">Soovitatavad süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="69e07-183">Recommended system requirements</span></span>

-   <span data-ttu-id="69e07-184">6 GB RAM-i</span><span class="sxs-lookup"><span data-stu-id="69e07-184">6 GB of RAM</span></span>
-   <span data-ttu-id="69e07-185">2,4 GHz i7 (või ekvivalent) CPU tippkiirus tuuma kohta (neli tuuma on soovitatavad).</span><span class="sxs-lookup"><span data-stu-id="69e07-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="69e07-186">Vähemalt 10 GB vaba ruumi (kanali andmebaas võib nõuda suurel hulgal ruumi)</span><span class="sxs-lookup"><span data-stu-id="69e07-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="69e07-187">Konnektori nõuded</span><span class="sxs-lookup"><span data-stu-id="69e07-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="69e07-188">Toetatud operatsioonisüsteemid</span><span class="sxs-lookup"><span data-stu-id="69e07-188">Supported operating systems</span></span>

-   <span data-ttu-id="69e07-189">Microsoft Dynamics AX-i konnektoril on kaks eraldi installiprogrammi: programm Async Server Connector service'i jaoks ja programm Real-time service for Dynamics AX 2012 R3 jaoks.</span><span class="sxs-lookup"><span data-stu-id="69e07-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="69e07-190">Mõlemad komponendid on 32-bitised rakendused, kuid töötavad nii x86- kui ka x64-põhistes arhitektuurides.</span><span class="sxs-lookup"><span data-stu-id="69e07-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="69e07-191">Mõlemaid komponente toetatakse järgmistes operatsioonisüsteemides.</span><span class="sxs-lookup"><span data-stu-id="69e07-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="69e07-192">Windows 7 Professionali, Enterprise’i ja Ultimate’i versioonides</span><span class="sxs-lookup"><span data-stu-id="69e07-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="69e07-193">Windows 8.1 Update 1 Professionali, Enterprise’i ja manustatud versioonid</span><span class="sxs-lookup"><span data-stu-id="69e07-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="69e07-194">Windows 10 Pro, Enterprise’i ja Enterprise LTSB versioonid</span><span class="sxs-lookup"><span data-stu-id="69e07-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="69e07-195">Microsoft Windows Server 2012 R2 ja Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="69e07-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="69e07-196">Minimaalsed süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="69e07-196">Minimum system requirements</span></span>
-   <span data-ttu-id="69e07-197">2 GB RAM, soovituslik 4 GB RAM</span><span class="sxs-lookup"><span data-stu-id="69e07-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="69e07-198">1,6 GHz CPU tippkiirus tuuma kohta (kaks tuuma minimaalselt.)</span><span class="sxs-lookup"><span data-stu-id="69e07-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="69e07-199">Vähemalt 10 GB vaba ruumi (kanali andmebaas võib nõuda suurel hulgal ruumi)</span><span class="sxs-lookup"><span data-stu-id="69e07-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="69e07-200">Arenduse nõuded kohalikes VM-ides</span><span class="sxs-lookup"><span data-stu-id="69e07-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="69e07-201">Kohalikes virtuaalmasinates (VM-id) arenduse nõuete kohta lisateabe saamiseks vaadake teemat [Asutusesiseselt töötav virtuaalmasin](../dev-tools/access-instances.md).</span><span class="sxs-lookup"><span data-stu-id="69e07-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="69e07-202">Vt ka</span><span class="sxs-lookup"><span data-stu-id="69e07-202">See also</span></span>

[<span data-ttu-id="69e07-203">Rakenduse Dynamics 365 for Finance and Operations, Enterprise Editioni hindamiskoopia hankimine</span><span class="sxs-lookup"><span data-stu-id="69e07-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

