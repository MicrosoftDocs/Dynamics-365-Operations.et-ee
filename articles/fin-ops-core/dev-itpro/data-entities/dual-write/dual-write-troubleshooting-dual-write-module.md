---
title: Topeltkirjutamise probleemide tõrkeotsing Finance and Operationsi rakendustes
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada Finance and Operationsi rakenduste topelkirjutuse mooduliga seotud probleeme.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 3ffeb2de0acc1761bccf62a1a124852c504e2a3a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131241"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a><span data-ttu-id="04963-103">Topeltkirjutamise probleemide tõrkeotsing Finance and Operationsi rakendustes</span><span class="sxs-lookup"><span data-stu-id="04963-103">Troubleshoot dual-write issues in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="04963-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="04963-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="04963-105">Täpsemalt annab see teema tõrkeotsingu teavet, mis aitab lahendada Finance and Operationsi rakenduste **Topelkirjutuse** mooduliga seotud probleeme.</span><span class="sxs-lookup"><span data-stu-id="04963-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04963-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="04963-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="04963-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="04963-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="04963-108">Te ei saa laadida topeltkirjutuse moodulit Finance and Operationsi rakenduses</span><span class="sxs-lookup"><span data-stu-id="04963-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="04963-109">Kui te ei saa avada lehte **Topeltkirjutus**, valides tööruumis **Andmehaldus** paani **Topeltkirjutus**, on andmete integratsiooni teenus tõenäoliselt maas.</span><span class="sxs-lookup"><span data-stu-id="04963-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="04963-110">Looge tugiteenusepilet andmete integratsiooni teenuse taaskäivitamise taotlemiseks.</span><span class="sxs-lookup"><span data-stu-id="04963-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-table-map"></a><span data-ttu-id="04963-111">Tõrge uue tabeli vastenduse loomise katsel</span><span class="sxs-lookup"><span data-stu-id="04963-111">Error when you try to create a new table map</span></span>

<span data-ttu-id="04963-112">**Probleemi lahendamiseks nõutav identimisteave:** sama kasutaja, kes topeltkirjutuse seadistas.</span><span class="sxs-lookup"><span data-stu-id="04963-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="04963-113">Teile võidakse kuvada järgmine tõrketeade, kui proovite konfigureerida uut tabelit topeltkirjutuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="04963-113">You might receive the following error message when you try to configure a new table for dual-write.</span></span> <span data-ttu-id="04963-114">Vastendust võib luua ainult kasutaja, kes seadistas topeltkirjutuse ühenduse.</span><span class="sxs-lookup"><span data-stu-id="04963-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="04963-115">*Vastuse oleku kood ei näita edu: 401 (autoriseerimata)*</span><span class="sxs-lookup"><span data-stu-id="04963-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="04963-116">Tõrge topeltkirjutuse kasutajaliidese avamisel</span><span class="sxs-lookup"><span data-stu-id="04963-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="04963-117">Teile võidakse kuvada järgmine tõrketeade, kui püüate tööruumist **Andmehaldus** topeltkirjutusele juurde pääseda.</span><span class="sxs-lookup"><span data-stu-id="04963-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="04963-118">*login.microsoftonline.com keeldus ühenduse loomisest.*</span><span class="sxs-lookup"><span data-stu-id="04963-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="04963-119">Probleemi lahendamiseks logige sisse Microsoft Edge InPrivate-aknas, Chromiumi inkognito-aknas või Google Chrome'i inkognito-aknas.</span><span class="sxs-lookup"><span data-stu-id="04963-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="04963-120">Samuti peate kolmanda osapoolte küpsiste blokeerimise tühistama või tühjendama.</span><span class="sxs-lookup"><span data-stu-id="04963-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a><span data-ttu-id="04963-121">Tõrge keskkonna linkimisel topeltkirjutusega või uue tabeli vastendamisel</span><span class="sxs-lookup"><span data-stu-id="04963-121">Error when you link the environment for dual-write or add a new table mapping</span></span>

<span data-ttu-id="04963-122">**Probleemi lahendamiseks nõutav roll:** nii Finance and Operationsi rakenduste kui ka teenuse Dataverse süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="04963-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="04963-123">Vastenduste linkimisel või loomisel võib ilmneda järgmine tõrge.</span><span class="sxs-lookup"><span data-stu-id="04963-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="04963-124">*Vastuse oleku kood ei näita edu: 403 (tokenexchange).<br> Seansi ID: \<your session id\><br> Juurtegevuse ID: \<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="04963-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="04963-125">See tõrge võib ilmneda juhul, kui teil pole topeltkirjutuse või vastenduste loomiseks piisavaid lube.</span><span class="sxs-lookup"><span data-stu-id="04963-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="04963-126">See tõrge võib ilmneda ka siis, kui teenuse Dataverse keskkond lähtestati ilma topeltkirjutuse linkimist tühistamata.</span><span class="sxs-lookup"><span data-stu-id="04963-126">This error can also occur if the Dataverse environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="04963-127">Keskkondi saavad linkida kõik kasutajad, kes on süsteemiadministraatorid nii Finance and Operationsi rakendustes kui ka teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="04963-127">Any user with system administrator role in both Finance and Operations apps and Dataverse can link the environments.</span></span> <span data-ttu-id="04963-128">Uusi tabeli vastendusi saavad lisada ainult kasutajad, kes seadistasid topeltkirjutuse ühenduse.</span><span class="sxs-lookup"><span data-stu-id="04963-128">Only the user who setup the dual-write connection can add new table maps.</span></span> <span data-ttu-id="04963-129">Pärast seadistamist saab iga süsteemiadministraatori rolliga kasutaja olekut jälgida ja vastendusi redigeerida.</span><span class="sxs-lookup"><span data-stu-id="04963-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-table-mapping"></a><span data-ttu-id="04963-130">Tõrge tabeli vastendamise peatamisel</span><span class="sxs-lookup"><span data-stu-id="04963-130">Error when you stop the table mapping</span></span>

<span data-ttu-id="04963-131">Kui proovite peatada tabeli vastendust, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="04963-131">You might receive the following error message when you try to stop the table mappings:</span></span>

<span data-ttu-id="04963-132">*\[Keelatud\], \[{„olek”:403,„allikas”:„”,„sõnum”:„Loa vahetuse tõrge: kasutajal pole juurdepääsu ühendusele dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx”}\], Kaugserver tagastas tõrke: (403) keelatud.*</span><span class="sxs-lookup"><span data-stu-id="04963-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="04963-133">See tõrge ilmneb siis, kui lingitud Dataverse'i keskkond ei ole saadaval.</span><span class="sxs-lookup"><span data-stu-id="04963-133">This error occurs when the linked Dataverse environment isn't available.</span></span>

<span data-ttu-id="04963-134">Probleemi lahendamiseks looge andmeintegratsiooni meeskonnale pilet.</span><span class="sxs-lookup"><span data-stu-id="04963-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="04963-135">Manustage võrgujälitus, et andmeintegratsiooni meeskond saaks märgistada vastendused olekusse **Ei tööta** tagaserveris.</span><span class="sxs-lookup"><span data-stu-id="04963-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-a-table-mapping"></a><span data-ttu-id="04963-136">Tabeli vastendamise alustamise katsel ilmnes tõrge</span><span class="sxs-lookup"><span data-stu-id="04963-136">Error while trying to start a table mapping</span></span>

<span data-ttu-id="04963-137">Kui proovite seada vastenduse olekut väärtusele **Töötab**, võite saada järgmise tõrketeate.</span><span class="sxs-lookup"><span data-stu-id="04963-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="04963-138">*Esialgset andmete sünkroonimist ei saa lõpule viia. Tõrge: topeltkirjutuse tõrge – lisandmooduli registreerimine nurjus: topeltkirjutuse otsingu metaandmete koostamine pole võimalik. Tõrkeobjekti viide pole seatud objekti eksemplarile.*</span><span class="sxs-lookup"><span data-stu-id="04963-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="04963-139">Selle tõrke parandus sõltub tõrke põhjusest.</span><span class="sxs-lookup"><span data-stu-id="04963-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="04963-140">Kui vastendusel on sõltuvaid vastendusi, siis veenduge, et selle tabeli vastendusest sõltuvad vastendused oleksid lubatud.</span><span class="sxs-lookup"><span data-stu-id="04963-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this table mapping.</span></span>
+ <span data-ttu-id="04963-141">Vastendusel võivad puududa lähte- või sihtveerud.</span><span class="sxs-lookup"><span data-stu-id="04963-141">The mapping might be missing source or destination columns.</span></span> <span data-ttu-id="04963-142">Kui veerg Finance and Operationsi rakenduses puuudb, järgige jaotises [Puuduva tabeli veeru probleem vastendusel](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) toodud samme.</span><span class="sxs-lookup"><span data-stu-id="04963-142">If a column in the Finance and Operations app is missing, then follow the steps in the section [Missing table columns issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps).</span></span> <span data-ttu-id="04963-143">Kui veerg on teenuses Dataverse puudu, klõpsake vastendusel nuppu **Värskenda tabeleid**, et veerud täidetaks vastenduses automaatselt.</span><span class="sxs-lookup"><span data-stu-id="04963-143">If a column in Dataverse is missing, then click **Refresh tables** button on the mapping so that the columns are automatically populated back into the mapping.</span></span>
