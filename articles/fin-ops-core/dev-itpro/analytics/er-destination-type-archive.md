---
title: ER-i sihtkoha tüübi arhiveerimine
description: See teema annab teavet selle kohta, kuidas iga elektroonilise aruandluse (ER) vormingu KAUST või FAIL komponenti arhiivimissihtkoha jaoks konfigureerida.
author: NickSelin
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 079eda04fcc41fc637419a83452db10b89ed1ab9
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894024"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="737b1-103">ER-i sihtkoha tüübi arhiveerimine</span><span class="sxs-lookup"><span data-stu-id="737b1-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="737b1-104">Saate konfigureerida arhiivi sihtkoha iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga **kausta** või **faili** komponendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="737b1-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="737b1-105">Sihtkoha sätte põhjal talletatakse loodud dokument ER tööde loendi kirje manusena.</span><span class="sxs-lookup"><span data-stu-id="737b1-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="737b1-106">Tulemuste vaatamiseks avage jaotis **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse tööd**.</span><span class="sxs-lookup"><span data-stu-id="737b1-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="737b1-107">Selle valiku abil saab saata loodud dokumendi Microsoft SharePointi kausta või Microsoft Azure’i salvestusruumi.</span><span class="sxs-lookup"><span data-stu-id="737b1-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="737b1-108">Määrake valiku **Lubatud** väärtuseks **Jah** väljundi saatmiseks valitud dokumenditüübiga määratletud sihtkohta.</span><span class="sxs-lookup"><span data-stu-id="737b1-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="737b1-109">Valida saab ainult neid dokumenditüüpe, millel grupiks on määratud **Fail**.</span><span class="sxs-lookup"><span data-stu-id="737b1-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="737b1-110">Dokumendi [tüübid](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) saate määratleda jaotistes **Organisatsiooni haldus**\>  **Dokumendihaldus**\> **Dokumenditüübid**.</span><span class="sxs-lookup"><span data-stu-id="737b1-110">You define document [types](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="737b1-111">ER-i sihtkohtade konfiguratsioon on sama, mis dokumendihaldussüsteemi konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="737b1-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="737b1-112">[![Leht Dokumenditüübid](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="737b1-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="737b1-113">Asukoht määrab, kuhu fail salvestatakse.</span><span class="sxs-lookup"><span data-stu-id="737b1-113">The location determines where the file is saved.</span></span> <span data-ttu-id="737b1-114">Kui sihtkoht **Arhiiv** on lubatud, saab konfiguratsiooni käivitamise tulemused salvestada tööarhiivi.</span><span class="sxs-lookup"><span data-stu-id="737b1-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="737b1-115">Tulemusi saate vaadata jaotises **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse arhiivitud tööd**.</span><span class="sxs-lookup"><span data-stu-id="737b1-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="737b1-116">Tööarhiivi jaoks saate dokumenditüübi valida, liikudes jaotisesse **Organisatsiooni haldus** \> **Tööruumid** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="737b1-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="737b1-117">Lisateabe saamiseks vt teemat [Elektroonilise aruandluse (ER) raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="737b1-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="737b1-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="737b1-118">SharePoint</span></span>

<span data-ttu-id="737b1-119">Faili saab salvestada selleks mõeldud SharePointi kausta.</span><span class="sxs-lookup"><span data-stu-id="737b1-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="737b1-120">SharePointi vaikeserveri määratlemiseks avage **Organisatsiooni haldus**\> **Dokumendihaldus**\> **Dokumendihalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="737b1-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="737b1-121">Vahekaardil **SharePoint** konfigureerige SharePointi kaust.</span><span class="sxs-lookup"><span data-stu-id="737b1-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="737b1-122">Seejärel saate valida selle kausta, kuhu ER väljund salvestatakse.</span><span class="sxs-lookup"><span data-stu-id="737b1-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="737b1-123">Selle dokumenditüübi **SharePoint** i asukoht peab olema valitud.</span><span class="sxs-lookup"><span data-stu-id="737b1-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="737b1-124">[![SharePointi kausta valimine](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="737b1-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="737b1-125">Azure’i salvestusruum</span><span class="sxs-lookup"><span data-stu-id="737b1-125">Azure Storage</span></span>

<span data-ttu-id="737b1-126">Kui dokumenditüübi asukohaks on määratud **Azure'i salvestusruum**, saate faili salvestada Azure’i salvestusruumi.</span><span class="sxs-lookup"><span data-stu-id="737b1-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="737b1-127">ER-i raamistik salvestab failid püsivalt Azure’i bloobimällu, erinevalt andmehaldusraamistikule, mis rakendab seitsmepäevast dokumentide säilituspoliitikat dokumentidele, mis tuleb töödelda.</span><span class="sxs-lookup"><span data-stu-id="737b1-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="737b1-128">Lisateabe saamiseks vt teemat [Olekusõnumi olekute läheduses](../data-entities/recurring-integrations.md#api-for-getting-message-status)ja [Oleku kontrollimise API](../data-entities/data-management-api.md#status-check-api).</span><span class="sxs-lookup"><span data-stu-id="737b1-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="737b1-129">ER-ga seotud failid talletatakse Azure’i bloobimälus vastavate tabeli kirjete manustena nii kaua kui vajalik.</span><span class="sxs-lookup"><span data-stu-id="737b1-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="737b1-130">Aure’i bloobimälust kustutatakse üks fail koos rakenduse tabeli kirjega, millele see fail oli manustatud.</span><span class="sxs-lookup"><span data-stu-id="737b1-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="737b1-131">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="737b1-131">Additional resources</span></span>

- [<span data-ttu-id="737b1-132">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="737b1-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="737b1-133">Elektroonilise aruandluse (ER) sihtkohad</span><span class="sxs-lookup"><span data-stu-id="737b1-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="737b1-134">Dokumendihalduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="737b1-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]