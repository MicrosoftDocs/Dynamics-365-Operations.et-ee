---
title: Süsteeminõuded
description: Selles artiklis kirjeldatakse rakenduse Microsoft Dynamics 365 Human Resources nõudeid.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f86cd60466661c87d762f2e2f0765b92351ee2b8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053583"
---
# <a name="system-requirements"></a><span data-ttu-id="b854e-103">Süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="b854e-103">System requirements</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b854e-104">Selles artiklis kirjeldatakse rakenduse Microsoft Dynamics 365 Human Resources nõudeid.</span><span class="sxs-lookup"><span data-stu-id="b854e-104">This article describes requirements for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b854e-105">Lisaks tuuakse välja riigid ja piirkonnad, kus rakendus Human Resources on saadaval ning teave keelte ja Human Resourcesi andmete lokaliseerimise kohta.</span><span class="sxs-lookup"><span data-stu-id="b854e-105">It also outlines the countries and regions where Human Resources is available, and information about languages and localization for Human Resources data.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="b854e-106">Toetatud veebibrauserid</span><span class="sxs-lookup"><span data-stu-id="b854e-106">Supported web browsers</span></span>

<span data-ttu-id="b854e-107">Rakendust Human Resources saab kasutada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemis.</span><span class="sxs-lookup"><span data-stu-id="b854e-107">Human Resources can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="b854e-108">Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s</span><span class="sxs-lookup"><span data-stu-id="b854e-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="b854e-109">Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7</span><span class="sxs-lookup"><span data-stu-id="b854e-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="b854e-110">Google Chrome (viimane avalikult saadaolev versioon)</span><span class="sxs-lookup"><span data-stu-id="b854e-110">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="b854e-111">Apple Safari (viimane avalikult saadaolev versioon)</span><span class="sxs-lookup"><span data-stu-id="b854e-111">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="b854e-112">Iga veebibrauseri uusima versiooni leidmiseks minge tarkvaratootja veebisaidile.</span><span class="sxs-lookup"><span data-stu-id="b854e-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="b854e-113">Tegevuse salvestajas loodud piltide jäädvustamiseks ja nende Microsoft Wordi dokumentidesse lisamiseks peab teil olema installitud Chrome’i laiendus.</span><span class="sxs-lookup"><span data-stu-id="b854e-113">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="b854e-114">Töövooredaktor käivitatakse ClickOnce’i rakendusena.</span><span class="sxs-lookup"><span data-stu-id="b854e-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="b854e-115">Ainult Microsoft Edge ja Internet Explorer (Microsoft Windowsi toetatud versioonis) toetavad ClickOnce’i rakendusi.</span><span class="sxs-lookup"><span data-stu-id="b854e-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="b854e-116">Töövooredaktori ClickOnce rakendus nõuab ühilduvat 64-bitist operatsioonisüsteemi.</span><span class="sxs-lookup"><span data-stu-id="b854e-116">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="b854e-117">PDF-failide eelvaateks soovitame kasutada tänapäevasi brausereid, nagu Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s või Chrome (viimane avalikult saadaolev versioon) Windows 10-s, Windows 8.1-s, Windows 8-s, Windows 7-s või tahvelarvutis Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="b854e-117">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="b854e-118">Võrgunõuded</span><span class="sxs-lookup"><span data-stu-id="b854e-118">Network requirements</span></span>
> * <span data-ttu-id="b854e-119">Human Resources on mõeldud võrkudele, mille latentsus on kuni 250–300 millisekundit (ms).</span><span class="sxs-lookup"><span data-stu-id="b854e-119">Human Resources is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="b854e-120">See on latentsus brauserikliendist Microsoft Azure’i andmekeskusse, mis majutab rakendust Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b854e-120">This is the latency from a browser client to the Microsoft Azure data center that hosts Human Resources.</span></span> <span data-ttu-id="b854e-121">Soovitame teilt testida võrgulatentsust veebiaadressil [www.azurespeed.com](https://www.azurespeed.com "Azure’i latentsustest").</span><span class="sxs-lookup"><span data-stu-id="b854e-121">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="b854e-122">Ribalaiuse nõuded rakenduse Human Resources puhul sõltuvad teie stsenaariumist.</span><span class="sxs-lookup"><span data-stu-id="b854e-122">Bandwidth requirements for Human Resources depend on your scenario.</span></span> <span data-ttu-id="b854e-123">Kõige tüüpilisemad stsenaariumid nõuavad ribalaiust rohkem kui 50 kilobaiti sekundis (KB/s).</span><span class="sxs-lookup"><span data-stu-id="b854e-123">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="b854e-124">Ärge arvutage ribalaiuse nõudeid kliendi asukohast, korrutades kasutajate arvu minimaalsete ribalaiuse nõuetega.</span><span class="sxs-lookup"><span data-stu-id="b854e-124">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="b854e-125">Antud asukoha samaaegset kasutust on väga keeruline arvutada.</span><span class="sxs-lookup"><span data-stu-id="b854e-125">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="b854e-126">Ribalaiuse nõuete pärast muret tundvad kliendid peaksid kasutama rakenduse Human Resources eelvaateversiooni.</span><span class="sxs-lookup"><span data-stu-id="b854e-126">For customers who are concerned about bandwidth requirements, use a trial version of Human Resources.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="b854e-127">Toetatud Microsoft Office’i rakendused</span><span class="sxs-lookup"><span data-stu-id="b854e-127">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="b854e-128">Microsoft Exceli ja Wordi lisandmoodulite käivitamiseks peab teil olema installitud Windowsile või Macile mõeldud Microsoft Office 2016.</span><span class="sxs-lookup"><span data-stu-id="b854e-128">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="b854e-129">Versiooninõuete kohta lisateabe saamiseks vaadake teemat [Office’i integratsiooni tõrkeotsing](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Office’i integreerimise tõrkeotsing").</span><span class="sxs-lookup"><span data-stu-id="b854e-129">For more details about version requirements, see [Office integration troubleshooting](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="b854e-130">Funktsiooniga Ekspordi Excelisse või Ekspordi Wordi loodud dokumentide vaatamiseks peab teil olema installitud Microsoft Office 2007 või uuem versioon.</span><span class="sxs-lookup"><span data-stu-id="b854e-130">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="b854e-131">Piirkondlik saadavus, keeled ja lokaliseerimine</span><span class="sxs-lookup"><span data-stu-id="b854e-131">Regional availability, languages, and localization</span></span>

<span data-ttu-id="b854e-132">Saate alla laadida PDF-faili riikide, piirkondade ja keelte kohta, mida Human Resources toetab teemast [Microsoft Dynamics 365 rahvusvaheline kättesaadavus](/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="b854e-132">You can download a PDF file of the countries, regions, and languages Human Resources supports at [International availability of Microsoft Dynamics 365](/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="b854e-133">Kui kasutajaliides on lokaliseeritud teistesse keeltesse, talletatakse kõik kasutajaandmed keeles, milles need sisestati.</span><span class="sxs-lookup"><span data-stu-id="b854e-133">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="b854e-134">Saate luua e-kirju ja malle teistes keeltes, kuid sellised andmed nagu planeerimise teave on praegu saadaval ainult inglise keeles.</span><span class="sxs-lookup"><span data-stu-id="b854e-134">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="b854e-135">Kui olete arendaja, kes on huvitatud riigi- või piirkonnapõhiste kohanduste loomisest või luua lahendus mõnele riigile või piirkonnale, mida Microsoft praegu ei toeta, vt [Globaliseerumine](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="b854e-135">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]