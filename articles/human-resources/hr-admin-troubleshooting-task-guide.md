---
title: Tegevuse juhiste salvestamine LCS-i ja nende taasesitamine
description: Selles artiklis selgitatakse, kuidas salvestada tegevusjuhiseid teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja neid seejärel taasesitada.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a18bb14ba8c3c926065c97b0ee26c38ee86ded2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053271"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="40cbf-103">Tegevuse juhiste salvestamine LCS-i ja nende taasesitamine</span><span class="sxs-lookup"><span data-stu-id="40cbf-103">Save task guides to LCS and replay them</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="40cbf-104">**Keskkonna üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="40cbf-104">**Environment details**</span></span> 

<span data-ttu-id="40cbf-105">Microsoft Dynamics 365 Human Resources, mis on juurutatud teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu</span><span class="sxs-lookup"><span data-stu-id="40cbf-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="40cbf-106">**Väljasta**</span><span class="sxs-lookup"><span data-stu-id="40cbf-106">**Issue**</span></span>

<span data-ttu-id="40cbf-107">Klient soovib salvestada uusi tegevuse salvestisi oma LCS-i projekti ja seejärel salvestatud tegevuse juhiseid taasesitada.</span><span class="sxs-lookup"><span data-stu-id="40cbf-107">The customer wants to save new task recordings to the LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="40cbf-108">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="40cbf-108">**Resolution**</span></span>

<span data-ttu-id="40cbf-109">Tegevuse salvestise salvestamiseks LCS-i tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="40cbf-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="40cbf-110">Logige LCS-i sisse ja valige projekt.</span><span class="sxs-lookup"><span data-stu-id="40cbf-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="40cbf-111">Valige paan **Äriprotsesside modelleerija**.</span><span class="sxs-lookup"><span data-stu-id="40cbf-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="40cbf-112">Vaadake lehte jaotises Värskendatud BPM-kogemus.</span><span class="sxs-lookup"><span data-stu-id="40cbf-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="40cbf-113">Valige teek ja valige seejärel **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="40cbf-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="40cbf-114">Sisestage äriprotsesside modelleerija (BPM) mudeli jaoks nimi.</span><span class="sxs-lookup"><span data-stu-id="40cbf-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="40cbf-115">Logige rakendusse Human Resources teenuses LCS sisse.</span><span class="sxs-lookup"><span data-stu-id="40cbf-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="40cbf-116">Sisestage väljale **Otsing** suvand **spikker**.</span><span class="sxs-lookup"><span data-stu-id="40cbf-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="40cbf-117">Teenuse Lifecycle Services spikker on avatud.</span><span class="sxs-lookup"><span data-stu-id="40cbf-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="40cbf-118">Valige teenuse Lifecycle Services spikri konfiguratsiooni jaoks nupp **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="40cbf-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="40cbf-119">Ilmuma peaks uus aktiivsena kuvatav BPM-i teek.</span><span class="sxs-lookup"><span data-stu-id="40cbf-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="40cbf-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="40cbf-120">Close the page.</span></span>
10. <span data-ttu-id="40cbf-121">Looge tegevuse salvestis.</span><span class="sxs-lookup"><span data-stu-id="40cbf-121">Create a task recording.</span></span>
11. <span data-ttu-id="40cbf-122">Kui olete lõpetanud, valige **Salvesta teenusesse Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="40cbf-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Salvesta teenustesse Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="40cbf-124">Valige BPM-i teek ja sõlm, kuhu tegevuse salvestis salvestada.</span><span class="sxs-lookup"><span data-stu-id="40cbf-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="40cbf-125">Tegevuse juhise taasesitamiseks LCS-ist tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="40cbf-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="40cbf-126">Käivitage tegevuse salvestaja.</span><span class="sxs-lookup"><span data-stu-id="40cbf-126">Start Task recorder.</span></span>
2. <span data-ttu-id="40cbf-127">Valige **Ava LCS-ist**.</span><span class="sxs-lookup"><span data-stu-id="40cbf-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="40cbf-128">Valige salvestatud tegevuse juhist omavad teek ja BPM-i sõlm.</span><span class="sxs-lookup"><span data-stu-id="40cbf-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="40cbf-129">Avage tegevuse juhis.</span><span class="sxs-lookup"><span data-stu-id="40cbf-129">Open the task guide.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]