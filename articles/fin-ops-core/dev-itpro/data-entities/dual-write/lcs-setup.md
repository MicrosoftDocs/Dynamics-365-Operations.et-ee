---
title: Topeltkirjutuse häälestus teenustest Lifecycle Services
description: Selles teemas selgitatakse, kuidas häälestada topeltkirjutuse ühendust teenusest Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103565"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="f7d49-103">Topeltkirjutuse häälestus teenustest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="f7d49-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f7d49-104">Selles teemas selgitatakse, kuidas häälestada topeltkirjutuse ühendust teenusest Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f7d49-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f7d49-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="f7d49-105">Prerequisites</span></span>

<span data-ttu-id="f7d49-106">Integratsiooni peate lõpule Power Platform viima järgmistes teemades kirjeldatud viisil:</span><span class="sxs-lookup"><span data-stu-id="f7d49-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="f7d49-107">Power Platform Integreerimine – lubage keskkonna juurutamisel</span><span class="sxs-lookup"><span data-stu-id="f7d49-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="f7d49-108">Power Platform Integreerimine – lubage keskkonna juurutamisel</span><span class="sxs-lookup"><span data-stu-id="f7d49-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="f7d49-109">Juhised topeltkirjutuse Dataverse häälestamiseks</span><span class="sxs-lookup"><span data-stu-id="f7d49-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="f7d49-110">Järgige neid samme LCS-i keskkonna üksikasjade lehel **topeltkirjutuse häälestamiseks** lehel:</span><span class="sxs-lookup"><span data-stu-id="f7d49-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="f7d49-111">Lehel **Keskkonna üksikasjad** laiendage jaotist **Power Platform Integratsioon** väljal.</span><span class="sxs-lookup"><span data-stu-id="f7d49-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="f7d49-112">Valige **topeltkirjutuse rakenduse** nupp.</span><span class="sxs-lookup"><span data-stu-id="f7d49-112">Select the **Dual-write application** button.</span></span>

    ![Power Platformi integratsioon](media/powerplat_integration_step2.png)

3. <span data-ttu-id="f7d49-114">Tingimustega nõustumiseks valige märkeruut **Konfigureeri**.</span><span class="sxs-lookup"><span data-stu-id="f7d49-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="f7d49-115">Jätkamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7d49-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="f7d49-116">Edenemist saate jälgida keskkonna üksikasjade lehte perioodiliselt värskendades.</span><span class="sxs-lookup"><span data-stu-id="f7d49-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="f7d49-117">Seadistus kestab tavaliselt 30 minutit või vähem.</span><span class="sxs-lookup"><span data-stu-id="f7d49-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="f7d49-118">Kui seadistus on lõpule viidud, teavitab teade teid, kas protsess õnnestus või kui see ebaõnnestus.</span><span class="sxs-lookup"><span data-stu-id="f7d49-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="f7d49-119">Kui seadistus nurjus, kuvatakse sellega seotud tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="f7d49-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="f7d49-120">Enne järgmisele astmele teisaldamist peate parandama kõik tõrked.</span><span class="sxs-lookup"><span data-stu-id="f7d49-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="f7d49-121">Valige **Linkige Power Platform keskkonnaga** et luua link rakenduse Dataverse ja käesoleva keskkonna andmebaasiga.</span><span class="sxs-lookup"><span data-stu-id="f7d49-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="f7d49-122">Seadistus kestab tavaliselt 5 minutit või vähem.</span><span class="sxs-lookup"><span data-stu-id="f7d49-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Link Power Platform keskkonda":::

8. <span data-ttu-id="f7d49-124">Kui linkimine on lõpetatud, kuvatakse hüperlink.</span><span class="sxs-lookup"><span data-stu-id="f7d49-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="f7d49-125">Logige lingi abil sisse topeltkirjutuse haldusalasse Finance and Operations keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="f7d49-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="f7d49-126">Sealt saate seadistada üksuse vastendamised.</span><span class="sxs-lookup"><span data-stu-id="f7d49-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="f7d49-127">Juhised topeltkirjutuse Dataverse häälestamiseks</span><span class="sxs-lookup"><span data-stu-id="f7d49-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="f7d49-128">Olemasoleva keskkonna topeltkirjutuse Dataverse häälestamiseks peate looma Microsofti [tugipileti](../../lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="f7d49-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="f7d49-129">Pilet peab sisaldama:</span><span class="sxs-lookup"><span data-stu-id="f7d49-129">The ticket must include:</span></span>

+ <span data-ttu-id="f7d49-130">Teie Finance and Operations keskkonna ID.</span><span class="sxs-lookup"><span data-stu-id="f7d49-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="f7d49-131">Teie keskkonna nimi rakendusest Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="f7d49-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="f7d49-132">Organisatsiooni Dataverse ID või Power Platform keskkonna ID Power Platform Halduskeskusest.</span><span class="sxs-lookup"><span data-stu-id="f7d49-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="f7d49-133">Taotlege oma piletis, et ID oleks integratsiooniks kasutatav Power Platform eksemplar.</span><span class="sxs-lookup"><span data-stu-id="f7d49-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="f7d49-134">LCS-i abil ei saa keskkondade linkimist tühistada.</span><span class="sxs-lookup"><span data-stu-id="f7d49-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="f7d49-135">Keskkonna linkimise tühistamiseks avage tööruum **Andmete integratsioon** keskkonnas Finance and Operations ja seejärel valige käsk **Tühista linkimine**.</span><span class="sxs-lookup"><span data-stu-id="f7d49-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
