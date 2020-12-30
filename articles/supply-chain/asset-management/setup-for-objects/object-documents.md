---
title: Vara dokumendid
description: Selles teemas selgitatakse vara dokumente varahalduses.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1e251dbbede23466109f6219671db7f62d6d420
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426167"
---
# <a name="asset-documents"></a><span data-ttu-id="ed306-103">Vara dokumendid</span><span class="sxs-lookup"><span data-stu-id="ed306-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ed306-104">Selles teemas selgitatakse vara dokumente varahalduses.</span><span class="sxs-lookup"><span data-stu-id="ed306-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="ed306-105">Varahalduses saate seadistada dokumente nii, et need oleksid automaatselt seotud näiteks töö tüüpide, vara tootjate, vara tüüpide või varadega.</span><span class="sxs-lookup"><span data-stu-id="ed306-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="ed306-106">See funktsioon on kasulik, kui antakse välja värskendatud dokumendiversioonid.</span><span class="sxs-lookup"><span data-stu-id="ed306-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="ed306-107">Sel juhul peate lihtsalt värskendatud dokumendi lisama standardasukohta, mida kasutate oma Supply Chain Managementi dokumentide jaoks, ja kinnitama dokumendi loodud vara dokumendikirjega.</span><span class="sxs-lookup"><span data-stu-id="ed306-107">In that case, you just have to put the updated document in the standard location that you use for your Supply Chain Management documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="ed306-108">Seejärel saab värskendatud dokumendile juurde pääseda menüü-üksustest **Kõik varad**, **Aktiivsed varad**, **Minu aktiivsed varad**, **Kõik töökäsud** ja **Aktiivsed töökäsu tööd**.</span><span class="sxs-lookup"><span data-stu-id="ed306-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="ed306-109">Dokumentide dokumendikirjele kinnitamise protsess kasutab standardset dokumenditöötluse süsteemi.</span><span class="sxs-lookup"><span data-stu-id="ed306-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="ed306-110">**Näide 1:** töö tüübiga seotud dokument võib kirjeldada selle töö tüübi protseduuri.</span><span class="sxs-lookup"><span data-stu-id="ed306-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="ed306-111">**Näide 2:** vara tüübi, tootja ja mudeli kombinatsiooniga seotud dokument võib olla valitud varatootja mudeli standardkäsiraamat.</span><span class="sxs-lookup"><span data-stu-id="ed306-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="ed306-112">Loo vara dokumendi seos</span><span class="sxs-lookup"><span data-stu-id="ed306-112">Create asset document relation</span></span>

1. <span data-ttu-id="ed306-113">Valige **Varahaldus**\>**Häälestus**\>**Vara dokumendid**.</span><span class="sxs-lookup"><span data-stu-id="ed306-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="ed306-114">Valige **Uus**, et luua vara dokumendikirje.</span><span class="sxs-lookup"><span data-stu-id="ed306-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="ed306-115">Sõltuvalt sellest, kui täpset seost te dokumendile soovite, tehke asjakohased valikud ühel või mitmel järgmistest väljadest: **Vara tüüp**, **Tootja**, **Mudel**, **Vara**, **Töö tüübi kategooria**, **Töö tüüp**, **Töö tüübi variant** ja **Töö vajadus**.</span><span class="sxs-lookup"><span data-stu-id="ed306-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="ed306-116">Väljadel **Töö tüübi variant** ja **Töö vajadus** saadaolevad suvandid sõltuvad teie valikust väljal **Töö tüüp**.</span><span class="sxs-lookup"><span data-stu-id="ed306-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ed306-117">Kui süsteem otsib dokumente, mis peaksid olema seotud vara või töökäsuga, vaatab varahaldus läbi kõik vara dokumendikirjed, et kontrollida võimalikku vastet.</span><span class="sxs-lookup"><span data-stu-id="ed306-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="ed306-118">Varahaldus kontrollib alati kõige spetsiifilisemat kombinatsiooni esimesena.</span><span class="sxs-lookup"><span data-stu-id="ed306-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="ed306-119">Teisisõnu kontrollib varahaldus esmalt **Töö nõuet** väli.</span><span class="sxs-lookup"><span data-stu-id="ed306-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="ed306-120">Kui vastet ei leita, otsib see vastet väljale **Töö tüübi varianti**.</span><span class="sxs-lookup"><span data-stu-id="ed306-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="ed306-121">Kui vastet ei leita, kontrollib see vastet väljale **Töö tüüp**.</span><span class="sxs-lookup"><span data-stu-id="ed306-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="ed306-122">Nagu näete lehe **Vara dokumendid** paigutuses, tähendab see käitumine, et kõige spetsiifilisema kombinatsiooni leidmiseks kontrollib varahaldus vaste leidmiseks iga kirjet paremalt vasakule.</span><span class="sxs-lookup"><span data-stu-id="ed306-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="ed306-123">Vara või töökäsuga võib seotud olla mitu dokumenti.</span><span class="sxs-lookup"><span data-stu-id="ed306-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="ed306-124">Vajaduse korral saate hooldustaset muuta hooldustaotluse või töökäsu puhul.</span><span class="sxs-lookup"><span data-stu-id="ed306-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="ed306-125">Valige suvand **Manused**.</span><span class="sxs-lookup"><span data-stu-id="ed306-125">Select **Attachments**.</span></span> <span data-ttu-id="ed306-126">Kuvatakse standardse **dokumenditöötluse** leht.</span><span class="sxs-lookup"><span data-stu-id="ed306-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="ed306-127">Seadistage dokumendid või märkmed, mis tuleks varadokumendi kirjega siduda.</span><span class="sxs-lookup"><span data-stu-id="ed306-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="ed306-128">Pärast dokumentide sidumist kuvatakse väljal **Manused** kirjega seotud dokumentide arv.</span><span class="sxs-lookup"><span data-stu-id="ed306-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>
