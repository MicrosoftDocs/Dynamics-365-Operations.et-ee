---
title: Topeltkirjutuse mooduli tõrkeotsingu probleemid Finance and Operationsi rakendustes
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 853791d5ffc1d92b9fbafa2acc13cd5543c38196
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275529"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="54c64-103">Topeltkirjutuse mooduli tõrkeotsingu probleemid Finance and Operationsi rakendustes</span><span class="sxs-lookup"><span data-stu-id="54c64-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54c64-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="54c64-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="54c64-105">Täpsemalt annab see teema tõrkeotsingu teavet, mis aitab lahendada Finance and Operationsi rakenduste **Topelkirjutuse** mooduliga seotud probleeme.</span><span class="sxs-lookup"><span data-stu-id="54c64-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="54c64-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="54c64-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="54c64-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="54c64-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="54c64-108">Te ei saa laadida topeltkirjutuse moodulit Finance and Operationsi rakenduses</span><span class="sxs-lookup"><span data-stu-id="54c64-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="54c64-109">Kui te ei saa avada lehte **Topeltkirjutus**, valides tööruumis **Andmehaldus** paani **Topeltkirjutus**, on andmete integratsiooni teenus tõenäoliselt maas.</span><span class="sxs-lookup"><span data-stu-id="54c64-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="54c64-110">Looge tugiteenusepilet andmete integratsiooni teenuse taaskäivitamise taotlemiseks.</span><span class="sxs-lookup"><span data-stu-id="54c64-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-map"></a><span data-ttu-id="54c64-111">Tõrge uue üksuse vastenduse loomise katsel</span><span class="sxs-lookup"><span data-stu-id="54c64-111">Error when you try to create a new entity map</span></span>

<span data-ttu-id="54c64-112">**Probleemi lahendamiseks nõutav identimisteave:** sama kasutaja, kes topeltkirjutuse seadistas.</span><span class="sxs-lookup"><span data-stu-id="54c64-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="54c64-113">Teile võidakse kuvada järgmine tõrketeade, kui proovite konfigureerida uut üksust topeltkirjutuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="54c64-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="54c64-114">Vastendust võib luua ainult kasutaja, kes seadistas topeltkirjutuse ühenduse.</span><span class="sxs-lookup"><span data-stu-id="54c64-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="54c64-115">*Vastuse oleku kood ei näita edu: 401 (autoriseerimata)*</span><span class="sxs-lookup"><span data-stu-id="54c64-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="54c64-116">Tõrge topeltkirjutuse kasutajaliidese avamisel</span><span class="sxs-lookup"><span data-stu-id="54c64-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="54c64-117">Teile võidakse kuvada järgmine tõrketeade, kui püüate tööruumist **Andmehaldus** topeltkirjutusele juurde pääseda.</span><span class="sxs-lookup"><span data-stu-id="54c64-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="54c64-118">*login.microsoftonline.com keeldus ühenduse loomisest.*</span><span class="sxs-lookup"><span data-stu-id="54c64-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="54c64-119">Probleemi lahendamiseks logige sisse Microsoft Edge InPrivate-aknas, Chromiumi inkognito-aknas või Google Chrome'i inkognito-aknas.</span><span class="sxs-lookup"><span data-stu-id="54c64-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="54c64-120">Samuti peate kolmanda osapoolte küpsiste blokeerimise tühistama või tühjendama.</span><span class="sxs-lookup"><span data-stu-id="54c64-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="54c64-121">Tõrge keskkonna linkimisel topeltkirjutusega või uue üksuse vastendamisel</span><span class="sxs-lookup"><span data-stu-id="54c64-121">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="54c64-122">**Probleemi lahendamiseks nõutav roll:** nii Finance and Operationsi rakenduste kui ka teenuse Common Data Service süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="54c64-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="54c64-123">Vastenduste linkimisel või loomisel võib ilmneda järgmine tõrge.</span><span class="sxs-lookup"><span data-stu-id="54c64-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="54c64-124">*Vastuse oleku kood ei näita edu: 403 (tokenexchange).<br> Seansi ID: \<teie seansi ID\><br> Juurtegevuse ID: \<teie juurtegevuse ID\>*</span><span class="sxs-lookup"><span data-stu-id="54c64-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="54c64-125">See tõrge võib ilmneda juhul, kui teil pole topeltkirjutuse või vastenduste loomiseks piisavaid lube.</span><span class="sxs-lookup"><span data-stu-id="54c64-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="54c64-126">See tõrge võib ilmneda ka siis, kui teenuse Common Data Service keskkond lähtestati ilma topeltkirjutuse linkimist tühistamata.</span><span class="sxs-lookup"><span data-stu-id="54c64-126">This error can also occur if the Common Data Service environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="54c64-127">Keskkondi saavad linkida kõik kasutajad, kes on süsteemiadministraatorid nii Finance and Operationsi rakendustes kui ka teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="54c64-127">Any user with system administrator role in both Finance and Operations apps and Common Data Service can link the environments.</span></span> <span data-ttu-id="54c64-128">Uusi üksuse vastendusi saavad lisada ainult kasutajad, kes seadistasid topeltkirjutuse ühenduse.</span><span class="sxs-lookup"><span data-stu-id="54c64-128">Only the user who setup the dual-write connection can add new entity maps.</span></span> <span data-ttu-id="54c64-129">Pärast seadistamist saab iga süsteemiadministraatori rolliga kasutaja olekut jälgida ja vastendusi redigeerida.</span><span class="sxs-lookup"><span data-stu-id="54c64-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="54c64-130">Tõrge üksuse vastendamise peatamisel</span><span class="sxs-lookup"><span data-stu-id="54c64-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="54c64-131">Kui proovite peatada vastendust, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="54c64-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="54c64-132">*\[Keelatud\], \[{„olek”:403,„allikas”:„”,„sõnum”:„Loa vahetuse tõrge: kasutajal pole juurdepääsu ühendusele dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx”}\], Kaugserver tagastas tõrke: (403) keelatud.*</span><span class="sxs-lookup"><span data-stu-id="54c64-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="54c64-133">See tõrge ilmneb siis, kui lingitud Common Data Service'i keskkond ei ole saadaval.</span><span class="sxs-lookup"><span data-stu-id="54c64-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="54c64-134">Probleemi lahendamiseks looge andmeintegratsiooni meeskonnale pilet.</span><span class="sxs-lookup"><span data-stu-id="54c64-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="54c64-135">Manustage võrgujälitus, et andmeintegratsiooni meeskond saaks märgistada vastendused olekusse **Ei tööta** tagaserveris.</span><span class="sxs-lookup"><span data-stu-id="54c64-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-entity-mapping"></a><span data-ttu-id="54c64-136">Üksuse vastendamise alustamise katsel ilmnes tõrge</span><span class="sxs-lookup"><span data-stu-id="54c64-136">Error while trying to start an entity mapping</span></span>

<span data-ttu-id="54c64-137">Kui proovite seada vastenduse olekut väärtusele **Töötab**, võite saada järgmise tõrketeate.</span><span class="sxs-lookup"><span data-stu-id="54c64-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="54c64-138">*Esialgset andmete sünkroonimist ei saa lõpule viia. Tõrge: topeltkirjutuse tõrge – lisandmooduli registreerimine nurjus: topeltkirjutuse otsingu metaandmete koostamine pole võimalik. Tõrkeobjekti viide pole seatud objekti eksemplarile.*</span><span class="sxs-lookup"><span data-stu-id="54c64-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="54c64-139">Selle tõrke parandus sõltub tõrke põhjusest.</span><span class="sxs-lookup"><span data-stu-id="54c64-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="54c64-140">Kui vastendusel on sõltuvaid vastendusi, siis veenduge, et selle üksuse vastendusest sõltuvad vastendused oleksid lubatud.</span><span class="sxs-lookup"><span data-stu-id="54c64-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this entity mapping.</span></span>
+ <span data-ttu-id="54c64-141">Vastendusel võivad puududa lähte- või sihtväljad.</span><span class="sxs-lookup"><span data-stu-id="54c64-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="54c64-142">Kui väli on puudu Finance and Operationsi rakenduses, järgige jaotises [Puuduva üksuse välja probleem vastendusel](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps) toodud samme.</span><span class="sxs-lookup"><span data-stu-id="54c64-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="54c64-143">Kui väli on puudu teenuses Common Data Service, klõpsake vastendusel nuppu **Värskenda üksuseid**, et väljad täidetaks vastenduses automaatselt.</span><span class="sxs-lookup"><span data-stu-id="54c64-143">If a field in Common Data Service is missing, then click **Refresh entities** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
