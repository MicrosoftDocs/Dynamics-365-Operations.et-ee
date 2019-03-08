---
title: Tegevuse juhiste salvestamine LCS-i ja nende taasesitamine
description: Selles teemas selgitatakse, kuidas salvestada tegevusjuhiseid teenusesse Microsoft Dynamics Lifecycle Services (LCS) ja neid seejärel taasesitada.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304070"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="14c14-103">Tegevuse juhiste salvestamine LCS-i ja nende taasesitamine</span><span class="sxs-lookup"><span data-stu-id="14c14-103">Save task guides to LCS and replay them</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="14c14-104">**Keskkonna üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="14c14-104">**Environment details**</span></span> 

<span data-ttu-id="14c14-105">Microsoft Dynamics 365 for Talent, mis on juurutatud teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu</span><span class="sxs-lookup"><span data-stu-id="14c14-105">Microsoft Dynamics 365 for Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="14c14-106">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="14c14-106">**Issue**</span></span>

<span data-ttu-id="14c14-107">Klient soovib salvestada uusi tegevuse salvestisi enda LCS-i projekti ja seejärel salvestatud tegevuse juhiseid taasesitada.</span><span class="sxs-lookup"><span data-stu-id="14c14-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="14c14-108">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="14c14-108">**Resolution**</span></span>

<span data-ttu-id="14c14-109">Tegevuse salvestise salvestamiseks LCS-i tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="14c14-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="14c14-110">Logige LCS-i sisse ja valige projekt.</span><span class="sxs-lookup"><span data-stu-id="14c14-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="14c14-111">Valige paan **Äriprotsesside modelleerija**.</span><span class="sxs-lookup"><span data-stu-id="14c14-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="14c14-112">Vaadake lehte jaotises Värskendatud BPM-kogemus.</span><span class="sxs-lookup"><span data-stu-id="14c14-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="14c14-113">Valige teek ja valige seejärel **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="14c14-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="14c14-114">Sisestage äriprotsesside modelleerija (BPM) mudeli jaoks nimi.</span><span class="sxs-lookup"><span data-stu-id="14c14-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="14c14-115">Logige LCS-ist sisse Talenti.</span><span class="sxs-lookup"><span data-stu-id="14c14-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="14c14-116">Sisestage väljale **Otsing** suvand **spikker**.</span><span class="sxs-lookup"><span data-stu-id="14c14-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="14c14-117">Teenuse Lifecycle Services spikker on avatud.</span><span class="sxs-lookup"><span data-stu-id="14c14-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="14c14-118">Valige teenuse Lifecycle Services spikri konfiguratsiooni jaoks nupp **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="14c14-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="14c14-119">Ilmuma peaks uus aktiivsena kuvatav BPM-i teek.</span><span class="sxs-lookup"><span data-stu-id="14c14-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="14c14-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="14c14-120">Close the page.</span></span>
10. <span data-ttu-id="14c14-121">Looge tegevuse salvestis.</span><span class="sxs-lookup"><span data-stu-id="14c14-121">Create a task recording.</span></span>
11. <span data-ttu-id="14c14-122">Kui olete lõpetanud, valige **Salvesta teenusesse Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="14c14-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Salvesta teenustesse Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="14c14-124">Valige BPM-i teek ja sõlm, kuhu tegevuse salvestis salvestada.</span><span class="sxs-lookup"><span data-stu-id="14c14-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="14c14-125">Tegevuse juhise taasesitamiseks LCS-ist tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="14c14-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="14c14-126">Käivitage tegevuse salvestaja.</span><span class="sxs-lookup"><span data-stu-id="14c14-126">Start Task recorder.</span></span>
2. <span data-ttu-id="14c14-127">Valige **Ava LCS-ist**.</span><span class="sxs-lookup"><span data-stu-id="14c14-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="14c14-128">Valige salvestatud tegevuse juhist omavad teek ja BPM-i sõlm.</span><span class="sxs-lookup"><span data-stu-id="14c14-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="14c14-129">Avage tegevuse juhis.</span><span class="sxs-lookup"><span data-stu-id="14c14-129">Open the task guide.</span></span>
