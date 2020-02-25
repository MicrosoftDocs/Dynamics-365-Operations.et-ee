---
title: ER-i sihtkoha tüübi arhiveerimine
description: Sellest teemast leiate teatevt, kuidas konfigureerida arhiivi sihtkoha iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga kausta või faili komponendi jaoks.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019728"
---
# <span data-ttu-id="f1118-103"><a name="ArchiveDestinationType">Arhiivi sihtkoht</a></span><span class="sxs-lookup"><span data-stu-id="f1118-103"><a name="ArchiveDestinationType">Archive destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1118-104">Saate konfigureerida arhiivi sihtkoha iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga kausta või faili komponendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="f1118-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="f1118-105">Sihtkoha sätte põhjal talletatakse loodud dokument ER tööde loendi kirje manusena.</span><span class="sxs-lookup"><span data-stu-id="f1118-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="f1118-106">Selle valiku abil saab saata loodud dokumendi Microsoft SharePointi kausta või Microsoft Azure’i salvestusruumi.</span><span class="sxs-lookup"><span data-stu-id="f1118-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="f1118-107">Määrake valiku **Lubatud** väärtuseks **Jah** väljundi saatmiseks valitud dokumenditüübiga määratletud sihtkohta.</span><span class="sxs-lookup"><span data-stu-id="f1118-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="f1118-108">Valida saab ainult neid dokumenditüüpe, millel grupiks on määratud **Fail**.</span><span class="sxs-lookup"><span data-stu-id="f1118-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="f1118-109">Dokumendi [tüübid](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) saate määratleda jaotistes **Organisatsiooni haldus**\>  **Dokumendihaldus**\> **Dokumenditüübid**.</span><span class="sxs-lookup"><span data-stu-id="f1118-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="f1118-110">ER-i sihtkohtade konfiguratsioon on sama, mis dokumendihaldussüsteemi konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="f1118-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="f1118-111">[![Leht Dokumenditüübid](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="f1118-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="f1118-112">Asukoht määrab, kuhu fail salvestatakse.</span><span class="sxs-lookup"><span data-stu-id="f1118-112">The location determines where the file is saved.</span></span> <span data-ttu-id="f1118-113">Kui sihtkoht **Arhiiv** on lubatud, saab konfiguratsiooni käivitamise tulemused salvestada tööarhiivi.</span><span class="sxs-lookup"><span data-stu-id="f1118-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="f1118-114">Tulemusi saate vaadata jaotises **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse arhiivitud tööd**.</span><span class="sxs-lookup"><span data-stu-id="f1118-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="f1118-115">Tööarhiivi jaoks saate dokumenditüübi valida, liikudes jaotisesse **Organisatsiooni haldus** \> **Tööruumid** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f1118-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="f1118-116">Lisateabe saamiseks vt teemat [Elektroonilise aruandluse (ER) raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="f1118-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="f1118-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="f1118-117">SharePoint</span></span>

<span data-ttu-id="f1118-118">Faili saab salvestada selleks mõeldud SharePointi kausta.</span><span class="sxs-lookup"><span data-stu-id="f1118-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="f1118-119">SharePointi vaikeserveri määratlemiseks avage **Organisatsiooni haldus**\> **Dokumendihaldus**\> **Dokumendihalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f1118-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="f1118-120">Vahekaardil **SharePoint** konfigureerige SharePointi kaust.</span><span class="sxs-lookup"><span data-stu-id="f1118-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="f1118-121">Seejärel saate valida selle kausta, kuhu ER väljund salvestatakse.</span><span class="sxs-lookup"><span data-stu-id="f1118-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="f1118-122">Selle dokumenditüübi **SharePoint**i asukoht peab olema valitud.</span><span class="sxs-lookup"><span data-stu-id="f1118-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="f1118-123">[![SharePointi kausta valimine](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="f1118-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="f1118-124">Azure’i salvestusruum</span><span class="sxs-lookup"><span data-stu-id="f1118-124">Azure Storage</span></span>

<span data-ttu-id="f1118-125">Kui dokumenditüübi asukohaks on määratud **Azure'i salvestusruum**, saate faili salvestada Azure’i salvestusruumi.</span><span class="sxs-lookup"><span data-stu-id="f1118-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1118-126">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f1118-126">Additional resources</span></span>

- [<span data-ttu-id="f1118-127">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="f1118-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f1118-128">Elektroonilise aruandluse (ER) sihtkohad</span><span class="sxs-lookup"><span data-stu-id="f1118-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="f1118-129">Dokumendihalduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f1118-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
