---
title: Tegevuse juhiste salvestamine LCS-i ja nende taasesitamine
description: Selles artiklis selgitatakse, kuidas salvestada tegevusjuhiseid teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja neid seejärel taasesitada.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d6102bafc9b55f9eff05bfc4a63c177c6548694
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463258"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="526a8-103">Tegevuse juhiste salvestamine LCS-i ja nende taasesitamine</span><span class="sxs-lookup"><span data-stu-id="526a8-103">Save task guides to LCS and replay them</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="526a8-104">**Keskkonna üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="526a8-104">**Environment details**</span></span> 

<span data-ttu-id="526a8-105">Microsoft Dynamics 365 Human Resources, mis on juurutatud teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu</span><span class="sxs-lookup"><span data-stu-id="526a8-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="526a8-106">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="526a8-106">**Issue**</span></span>

<span data-ttu-id="526a8-107">Klient soovib salvestada uusi tegevuse salvestisi enda LCS-i projekti ja seejärel salvestatud tegevuse juhiseid taasesitada.</span><span class="sxs-lookup"><span data-stu-id="526a8-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="526a8-108">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="526a8-108">**Resolution**</span></span>

<span data-ttu-id="526a8-109">Tegevuse salvestise salvestamiseks LCS-i tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="526a8-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="526a8-110">Logige LCS-i sisse ja valige projekt.</span><span class="sxs-lookup"><span data-stu-id="526a8-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="526a8-111">Valige paan **Äriprotsesside modelleerija**.</span><span class="sxs-lookup"><span data-stu-id="526a8-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="526a8-112">Vaadake lehte jaotises Värskendatud BPM-kogemus.</span><span class="sxs-lookup"><span data-stu-id="526a8-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="526a8-113">Valige teek ja valige seejärel **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="526a8-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="526a8-114">Sisestage äriprotsesside modelleerija (BPM) mudeli jaoks nimi.</span><span class="sxs-lookup"><span data-stu-id="526a8-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="526a8-115">Logige rakendusse Human Resources teenuses LCS sisse.</span><span class="sxs-lookup"><span data-stu-id="526a8-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="526a8-116">Sisestage väljale **Otsing** suvand **spikker**.</span><span class="sxs-lookup"><span data-stu-id="526a8-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="526a8-117">Teenuse Lifecycle Services spikker on avatud.</span><span class="sxs-lookup"><span data-stu-id="526a8-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="526a8-118">Valige teenuse Lifecycle Services spikri konfiguratsiooni jaoks nupp **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="526a8-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="526a8-119">Ilmuma peaks uus aktiivsena kuvatav BPM-i teek.</span><span class="sxs-lookup"><span data-stu-id="526a8-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="526a8-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="526a8-120">Close the page.</span></span>
10. <span data-ttu-id="526a8-121">Looge tegevuse salvestis.</span><span class="sxs-lookup"><span data-stu-id="526a8-121">Create a task recording.</span></span>
11. <span data-ttu-id="526a8-122">Kui olete lõpetanud, valige **Salvesta teenusesse Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="526a8-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Salvesta teenustesse Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="526a8-124">Valige BPM-i teek ja sõlm, kuhu tegevuse salvestis salvestada.</span><span class="sxs-lookup"><span data-stu-id="526a8-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="526a8-125">Tegevuse juhise taasesitamiseks LCS-ist tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="526a8-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="526a8-126">Käivitage tegevuse salvestaja.</span><span class="sxs-lookup"><span data-stu-id="526a8-126">Start Task recorder.</span></span>
2. <span data-ttu-id="526a8-127">Valige **Ava LCS-ist**.</span><span class="sxs-lookup"><span data-stu-id="526a8-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="526a8-128">Valige salvestatud tegevuse juhist omavad teek ja BPM-i sõlm.</span><span class="sxs-lookup"><span data-stu-id="526a8-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="526a8-129">Avage tegevuse juhis.</span><span class="sxs-lookup"><span data-stu-id="526a8-129">Open the task guide.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]