---
title: Rakenduse Talent süsteeminõuded ja värskenduspoliitika
description: Selles teemas on loetletud rakenduse Dynamics 365 for Talent nõuded. Samuti on välja toodud värskenduspoliitika.
author: andreabichsel
manager: AnnBe
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ea8b7485b142245a359648a2a85d2a3e2a6d6629
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517815"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="b051a-104">Rakenduse Talent süsteeminõuded ja värskenduspoliitika</span><span class="sxs-lookup"><span data-stu-id="b051a-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b051a-105">See teema kirjeldab rakendusele Microsoft Dynamics 365 for Talent, samuti rakendustele Attract, Onboard, ja Core HR esitatavaid nõudeid.</span><span class="sxs-lookup"><span data-stu-id="b051a-105">This topic describes requirements for Microsoft Dynamics 365 for Talent, including Attract, Onboard, and Core HR.</span></span> <span data-ttu-id="b051a-106">Tuuakse välja ka riigid ja piirkonnad, kus Talent on saadaval, lisaks teave keelte ja Talenti andmete lokaliseerimise kohta.</span><span class="sxs-lookup"><span data-stu-id="b051a-106">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="b051a-107">Lisaks pakub see teema Talenti värskenduspoliitikat.</span><span class="sxs-lookup"><span data-stu-id="b051a-107">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="b051a-108">Toetatud veebibrauserid</span><span class="sxs-lookup"><span data-stu-id="b051a-108">Supported web browsers</span></span>

<span data-ttu-id="b051a-109">Microsoft Dynamics 365 for Talenti veebirakendust saab kasutada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemis.</span><span class="sxs-lookup"><span data-stu-id="b051a-109">The Microsoft Dynamics 365 for Talent web application can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="b051a-110">Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s</span><span class="sxs-lookup"><span data-stu-id="b051a-110">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="b051a-111">Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7</span><span class="sxs-lookup"><span data-stu-id="b051a-111">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="b051a-112">Google Chrome (viimane avalikult saadaolev versioon)</span><span class="sxs-lookup"><span data-stu-id="b051a-112">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="b051a-113">Apple Safari (viimane avalikult saadaolev versioon)</span><span class="sxs-lookup"><span data-stu-id="b051a-113">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="b051a-114">Iga veebibrauseri uusima versiooni leidmiseks minge tarkvaratootja veebisaidile.</span><span class="sxs-lookup"><span data-stu-id="b051a-114">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="b051a-115">Tegevuse salvestajas loodud piltide jäädvustamiseks ja nende Microsoft Wordi dokumentidesse lisamiseks peab teil olema installitud Chrome’i laiendus.</span><span class="sxs-lookup"><span data-stu-id="b051a-115">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="b051a-116">Töövooredaktor käivitatakse ClickOnce’i rakendusena.</span><span class="sxs-lookup"><span data-stu-id="b051a-116">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="b051a-117">Ainult Microsoft Edge ja Internet Explorer (Microsoft Windowsi toetatud versioonis) toetavad ClickOnce’i rakendusi.</span><span class="sxs-lookup"><span data-stu-id="b051a-117">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="b051a-118">Töövooredaktori ClickOnce rakendus nõuab ühilduvat 64-bitist operatsioonisüsteemi.</span><span class="sxs-lookup"><span data-stu-id="b051a-118">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="b051a-119">PDF-failide eelvaateks soovitame kasutada tänapäevasi brausereid, nagu Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s või Chrome (viimane avalikult saadaolev versioon) Windows 10-s, Windows 8.1-s, Windows 8-s, Windows 7-s või tahvelarvutis Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="b051a-119">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="b051a-120">Võrgunõuded</span><span class="sxs-lookup"><span data-stu-id="b051a-120">Network requirements</span></span>
> * <span data-ttu-id="b051a-121">Dynamics 365 for Talent on mõeldud võrkudele, mille latentsus on kuni 250–300 millisekundit (ms).</span><span class="sxs-lookup"><span data-stu-id="b051a-121">Dynamics 365 for Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="b051a-122">See on latentsus brauserikliendist Microsoft Azure’i andmekeskusse, mis majutab rakendust Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="b051a-122">This is the latency from a browser client to the Microsoft Azure data center that hosts Dynamics 365 for Talent.</span></span> <span data-ttu-id="b051a-123">Soovitame teilt testida võrgulatentsust veebiaadressil [www.azurespeed.com](https://www.azurespeed.com "Azure’i latentsustest").</span><span class="sxs-lookup"><span data-stu-id="b051a-123">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="b051a-124">Ribalaiuse nõuded Dynamics 365 for Talenti puhul sõltuvad teie stsenaariumist.</span><span class="sxs-lookup"><span data-stu-id="b051a-124">Bandwidth requirements for Dynamics 365 for Talent depend on your scenario.</span></span> <span data-ttu-id="b051a-125">Kõige tüüpilisemad stsenaariumid nõuavad ribalaiust rohkem kui 50 kilobaiti sekundis (KB/s).</span><span class="sxs-lookup"><span data-stu-id="b051a-125">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="b051a-126">Ärge arvutage ribalaiuse nõudeid kliendi asukohast, korrutades kasutajate arvu minimaalsete ribalaiuse nõuetega.</span><span class="sxs-lookup"><span data-stu-id="b051a-126">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="b051a-127">Antud asukoha samaaegset kasutust on väga keeruline arvutada.</span><span class="sxs-lookup"><span data-stu-id="b051a-127">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="b051a-128">Ribalaiuse nõuete pärast muret tundvad kliendid peaksid kasutama rakenduse Dynamics 365 for Talent eelvaateversiooni.</span><span class="sxs-lookup"><span data-stu-id="b051a-128">For customers who are concerned about bandwidth requirements, use a trial version of Dynamics 365 for Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="b051a-129">Toetatud Microsoft Office’i rakendused</span><span class="sxs-lookup"><span data-stu-id="b051a-129">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="b051a-130">Microsoft Exceli ja Wordi lisandmoodulite käivitamiseks peab teil olema installitud Windowsile või Macile mõeldud Microsoft Office 2016.</span><span class="sxs-lookup"><span data-stu-id="b051a-130">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="b051a-131">Versiooninõuete kohta lisateabe saamiseks vaadake teemat [Office’i integratsiooni tõrkeotsing](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office’i integratsiooni tõrkeotsing").</span><span class="sxs-lookup"><span data-stu-id="b051a-131">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="b051a-132">Funktsiooniga Ekspordi Excelisse või Ekspordi Wordi loodud dokumentide vaatamiseks peab teil olema installitud Microsoft Office 2007 või uuem versioon.</span><span class="sxs-lookup"><span data-stu-id="b051a-132">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="b051a-133">Piirkondlik saadavus, keeled ja lokaliseerimine</span><span class="sxs-lookup"><span data-stu-id="b051a-133">Regional availability, languages, and localization</span></span>

<span data-ttu-id="b051a-134">Saate alla laadida PDF-faili riikide, piirkondade ja keelte kohta, mida Talent toetab siit [Microsoft Dynamics 365 rahvusvaheline kättesaadavus](https://docs.microsoft.com/dynamics365/get-started/availability)</span><span class="sxs-lookup"><span data-stu-id="b051a-134">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="b051a-135">Kui kasutajaliides on lokaliseeritud teistesse keeltesse, talletatakse kõik kasutajaandmed keeles, milles need sisestati.</span><span class="sxs-lookup"><span data-stu-id="b051a-135">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="b051a-136">Saate luua e-kirju ja malle teistes keeltes, kuid sellised andmed nagu planeerimise teave on praegu saadaval ainult inglise keeles.</span><span class="sxs-lookup"><span data-stu-id="b051a-136">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="b051a-137">Kui olete arendaja, kes on huvitatud riigi- või piirkonnapõhiste kohanduste loomisest või luua lahendus mõnele riigile või piirkonnale, mida Microsoft praegu ei toeta, vt [Globaliseerumine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="b051a-137">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

## <a name="update-policy"></a><span data-ttu-id="b051a-138">Värskenduspoliitika</span><span class="sxs-lookup"><span data-stu-id="b051a-138">Update policy</span></span>

<span data-ttu-id="b051a-139">Microsoft Dynamics 365 for Talenti pakutakse pilveteenusena.</span><span class="sxs-lookup"><span data-stu-id="b051a-139">Microsoft Dynamics 365 for Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="b051a-140">Microsoft värskendab rakendust Dynamics 365 for Talent pidevalt ja automaatselt.</span><span class="sxs-lookup"><span data-stu-id="b051a-140">Updates to Dynamics 365 for Talent are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="b051a-141">Värskendusi antakse välja regulaarselt ja need tehakse kättesaadavaks kõikides keskkondades.</span><span class="sxs-lookup"><span data-stu-id="b051a-141">Updates are released on a regular cadence and will be made to all environments.</span></span> <span data-ttu-id="b051a-142">Dynamics 365 for Talenti tugi põhineb [Microsofti toe elutsükli poliitikal](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsofi toe elutükkel"), kust leiate terviklikud ja ennustatavad juhised tootetoe saadavuse kohta.</span><span class="sxs-lookup"><span data-stu-id="b051a-142">Dynamics 365 for Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>
