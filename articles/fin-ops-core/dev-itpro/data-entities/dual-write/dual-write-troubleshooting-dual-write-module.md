---
title: Finance and Operationsi rakendustes topeltirjutuse mooduliga seotud probleemide tõrkeotsing
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
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172756"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="1d596-103">Finance and Operationsi rakendustes topeltirjutuse mooduliga seotud probleemide tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="1d596-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="1d596-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="1d596-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="1d596-105">Täpsemalt annab see teema tõrkeotsingu teavet, mis aitab lahendada Finance and Operationsi rakenduste **Topelkirjutuse** mooduliga seotud probleeme.</span><span class="sxs-lookup"><span data-stu-id="1d596-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d596-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="1d596-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="1d596-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="1d596-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="1d596-108">Te ei saa laadida topeltkirjutuse moodulit rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1d596-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="1d596-109">Kui te ei saa avada lehte **Topeltkirjutus**, valides tööruumis **Andmehaldus** paani **Topeltkirjutus**, on andmete integratsiooni teenus tõenäoliselt maas.</span><span class="sxs-lookup"><span data-stu-id="1d596-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="1d596-110">Looge tugiteenusepilet andmete integratsiooni teenuse taaskäivitamise taotlemiseks.</span><span class="sxs-lookup"><span data-stu-id="1d596-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="1d596-111">Tõrge uue üksuse vastenduse loomise katsel</span><span class="sxs-lookup"><span data-stu-id="1d596-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="1d596-112">**Probleemi lahendamiseks nõutav mandaat:** Azure AD rentniku admin</span><span class="sxs-lookup"><span data-stu-id="1d596-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="1d596-113">Teile võidakse kuvada järgmine tõrketeade, kui proovite konfigureerida uut üksust topeltkirjutuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="1d596-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="1d596-114">*Vastuse oleku kood ei näita edu: 401 (autoriseerimata)*</span><span class="sxs-lookup"><span data-stu-id="1d596-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="1d596-115">See tõrge ilmneb, sest ainult Azure AD rentniku administraator saab lisada uue üksuse vastendamist.</span><span class="sxs-lookup"><span data-stu-id="1d596-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="1d596-116">Probleemi lahendamiseks logigesisse rakendusse Finance and Operations kui Azure AD administraatori rentnik.</span><span class="sxs-lookup"><span data-stu-id="1d596-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="1d596-117">Peate minema lehele web.PowerApps.com ja kinnitama ühenduse uuesti.</span><span class="sxs-lookup"><span data-stu-id="1d596-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="1d596-118">Tõrge topeltkirjutuse kasutajaliidese avamisel</span><span class="sxs-lookup"><span data-stu-id="1d596-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="1d596-119">Teile võidakse kuvada järgmine tõrketeade, kui püüate tööruumist **Andmehaldus** topeltkirjutusele juurde pääseda.</span><span class="sxs-lookup"><span data-stu-id="1d596-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="1d596-120">*login.microsoftonline.com keeldus ühenduse loomisest.*</span><span class="sxs-lookup"><span data-stu-id="1d596-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="1d596-121">Probleemi lahendamiseks logige sisse Microsoft Edge InPrivate-aknas, Chromiumi inkognito-aknas või Google Chrome'i inkognito-aknas.</span><span class="sxs-lookup"><span data-stu-id="1d596-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="1d596-122">Samuti peate kolmanda osapoolte küpsiste blokeerimise tühistama või tühjendama.</span><span class="sxs-lookup"><span data-stu-id="1d596-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="1d596-123">Tõrge keskkonna linkimisel topeltkirjutusega või uue üksuse vastendamisel</span><span class="sxs-lookup"><span data-stu-id="1d596-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="1d596-124">**Probleemi lahendamiseks nõutav mandaat:** Azure AD rentniku admin</span><span class="sxs-lookup"><span data-stu-id="1d596-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="1d596-125">Vastenduste linkimisel või loomisel võib ilmneda järgmine tõrge.</span><span class="sxs-lookup"><span data-stu-id="1d596-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="1d596-126">*Vastuse oleku kood ei näita edu: 403 (tokenexchange).<br> Seansi ID: \<teie seansi ID\><br> Juurtegevuse ID: \<teie juurtegevuse ID\>*</span><span class="sxs-lookup"><span data-stu-id="1d596-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="1d596-127">See tõrge võib ilmneda juhul, kui teil pole topeltkirjutuse või vastenduste loomiseks piisavaid lube.</span><span class="sxs-lookup"><span data-stu-id="1d596-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="1d596-128">Keskkondade linkimiseks ja uute üksuste vastenduste lisamiseks peate kasutama Azure AD rentniku administraatorikontot.</span><span class="sxs-lookup"><span data-stu-id="1d596-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="1d596-129">Kuid pärast häälestust saate kasutada mitte-administraatori kontot oleku jälgimiseks ja vastenduste redigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="1d596-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="1d596-130">Tõrge üksuse vastendamise peatamisel</span><span class="sxs-lookup"><span data-stu-id="1d596-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="1d596-131">Kui proovite peatada vastendust, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="1d596-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="1d596-132">*\[Keelatud\], \[{„olek”:403,„allikas”:„”,„sõnum”:„Loa vahetuse tõrge: kasutajal pole juurdepääsu ühendusele dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx”}\], Kaugserver tagastas tõrke: (403) keelatud.*</span><span class="sxs-lookup"><span data-stu-id="1d596-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="1d596-133">See tõrge ilmneb siis, kui lingitud Common Data Service'i keskkond ei ole saadaval.</span><span class="sxs-lookup"><span data-stu-id="1d596-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="1d596-134">Probleemi lahendamiseks looge andmeintegratsiooni meeskonnale pilet.</span><span class="sxs-lookup"><span data-stu-id="1d596-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="1d596-135">Manustage võrgujälitus, et andmeintegratsiooni meeskond saaks märgistada vastendused olekusse **Ei tööta** tagaserveris.</span><span class="sxs-lookup"><span data-stu-id="1d596-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
