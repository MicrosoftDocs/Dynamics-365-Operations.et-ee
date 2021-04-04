---
title: Kasutajate importimine rakendusest Azure Active Directory
description: Süsteemiadministraatorid saavad seda toimingut kasutada valitud kasutajate käsitsi importimiseks või suure hulga kasutajate importimiseks Azure Active Directoryst.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c2600ad8f441e6b73b143c27afa08ad0a5c2748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571001"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="71c52-103">Kasutajate importimine rakendusest Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="71c52-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="71c52-104">Valitud kasutajate importimine</span><span class="sxs-lookup"><span data-stu-id="71c52-104">Import select users</span></span>

<span data-ttu-id="71c52-105">Süsteemiadministraatorid saavad seda toimingut kasutada valitud kasutajate importimiseks Azure Active Directoryst (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="71c52-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="71c52-106">Kasutaja imporditakse praeguse seansi ettevõttega kui nende vaikimisi ettevõte.</span><span class="sxs-lookup"><span data-stu-id="71c52-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="71c52-107">Kui see on kohaldatav, muutke praegust ettevõtet enne kasutajate importimist.</span><span class="sxs-lookup"><span data-stu-id="71c52-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="71c52-108">Minge jaotisse **Süsteemihaldus > Kasutajad > Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="71c52-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="71c52-109">Klõpsake **Impordi kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="71c52-109">Click **Import users**.</span></span>
4. <span data-ttu-id="71c52-110">Valige importimiseks kasutajad ja valige **Impordi kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="71c52-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="71c52-111">Pärast importimise lõpetamist on vaja kasutajatele määrata rollid.</span><span class="sxs-lookup"><span data-stu-id="71c52-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="71c52-112">Kasutajate hulgiimport</span><span class="sxs-lookup"><span data-stu-id="71c52-112">Import users in bulk</span></span>

<span data-ttu-id="71c52-113">Süsteemiadministraatorid saavad seda toimingut kasutada suure hulga kasutajate importimiseks Azure Active Directoryst.</span><span class="sxs-lookup"><span data-stu-id="71c52-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="71c52-114">Pange tähele, et partii importimise suvandit kasutades ei ole võimalik kasutajaid valida.</span><span class="sxs-lookup"><span data-stu-id="71c52-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="71c52-115">Partii tööna importimise käivitamine</span><span class="sxs-lookup"><span data-stu-id="71c52-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="71c52-116">Kasutaja imporditakse praeguse seansi ettevõttega kui nende vaikimisi ettevõte.</span><span class="sxs-lookup"><span data-stu-id="71c52-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="71c52-117">Kui see on kohaldatav, muutke praegust ettevõtet enne kasutajate importimist.</span><span class="sxs-lookup"><span data-stu-id="71c52-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="71c52-118">Minge jaotisse **Süsteemihaldus > Kasutajad > Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="71c52-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="71c52-119">Klõpsake suvandit **Partii import**.</span><span class="sxs-lookup"><span data-stu-id="71c52-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="71c52-120">Laiendage jaotist **Käivita taustal**.</span><span class="sxs-lookup"><span data-stu-id="71c52-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="71c52-121">Valige väärtus **Jah** väljal **Pakett-töötlus**.</span><span class="sxs-lookup"><span data-stu-id="71c52-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="71c52-122">Sisestage või valige väärtus väljal **Partiigrupp**.</span><span class="sxs-lookup"><span data-stu-id="71c52-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="71c52-123">See on valikuline etapp.</span><span class="sxs-lookup"><span data-stu-id="71c52-123">This is an optional step.</span></span>  
7. <span data-ttu-id="71c52-124">Valige väljal **Privaatne** väärtus **Jah**.</span><span class="sxs-lookup"><span data-stu-id="71c52-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="71c52-125">See on valikuline etapp.</span><span class="sxs-lookup"><span data-stu-id="71c52-125">This is an optional step.</span></span>  
8. <span data-ttu-id="71c52-126">Valige väljal **Kriitiline töö** väärtus **Jah**.</span><span class="sxs-lookup"><span data-stu-id="71c52-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="71c52-127">See on valikuline etapp.</span><span class="sxs-lookup"><span data-stu-id="71c52-127">This is an optional step.</span></span>  
9. <span data-ttu-id="71c52-128">Valige väljal **Jälgimiskategooria** soovitud suvand.</span><span class="sxs-lookup"><span data-stu-id="71c52-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="71c52-129">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="71c52-129">Click **OK**.</span></span>

<span data-ttu-id="71c52-130">Pärast importimise lõpetamist on vaja kasutajatele määrata rollid.</span><span class="sxs-lookup"><span data-stu-id="71c52-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="71c52-131">Liivakastikeskkonna käitamine</span><span class="sxs-lookup"><span data-stu-id="71c52-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="71c52-132">Valige **Partii import**.</span><span class="sxs-lookup"><span data-stu-id="71c52-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="71c52-133">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="71c52-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]