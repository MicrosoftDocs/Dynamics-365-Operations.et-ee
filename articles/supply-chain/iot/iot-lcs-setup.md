---
title: IoT iseõppimisvõime lisandmooduli installimine LCS-is
description: Selles teemas selgitatakse, kuidas installida IoT iseõppimisvõime lisandmoodulit teenuses Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad8b33633646f27bc368dc4bbedc1eb64c150a9f
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4426570"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="4ba15-103">IoT iseõppimisvõime lisandmooduli installimine LCS-is</span><span class="sxs-lookup"><span data-stu-id="4ba15-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4ba15-104">Selles teemas selgitatakse, kuidas installida IoT iseõppimisvõime lisandmoodulit teenuses Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4ba15-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="4ba15-105">Pange tähele, et lisandmooduleid ei saa installida demo/prooviversiooni keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="4ba15-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="4ba15-106">Enne lisandmooduli installimist peate [looma Azure'i ressursid](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="4ba15-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="4ba15-107">LCS-i keskkonna seadistamine</span><span class="sxs-lookup"><span data-stu-id="4ba15-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="4ba15-108">Avage LCS ja minge oma Microsoft Dynamics 365 Supply Chain Managementi keskkonda.</span><span class="sxs-lookup"><span data-stu-id="4ba15-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="4ba15-109">Kerige alla jaotiseni **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="4ba15-110">Valige **Installi uus lisandmoodul**, et kuvada selle keskkonna jaoks lubatud lisandmoodulite loend.</span><span class="sxs-lookup"><span data-stu-id="4ba15-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="4ba15-111">Valige dialoogiboksis **Installitava lisandmooduli valimine** suvand **IoT iseõppimisvõime**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="4ba15-112">Sisestage dialoogiboksis **Seadistuse lisandmoodul** oma IoT-keskuse ja Redis-vahemälu üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="4ba15-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="4ba15-113">Nõutavad väärtused leiate võtmehoidlast, mille lõite jaotises [Azure'i ressursside loomine](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="4ba15-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="4ba15-114">**Rentniku ID** – avage Azure'i portaali võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Ülevaade** ja kopeerige väärtus **Kausta ID**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="4ba15-115">Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="4ba15-116">**IoT sündmuste keskusega ühilduv lõpp-punkti võtmehoidla URI** – avage võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Ülevaade** ja kopeerige väärtus **DNS-i nimi**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="4ba15-117">Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="4ba15-118">**IoT sündmuste keskusega ühilduv lõpp-punkti saladuse nimi** – avage võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Saladused** ja kopeerige selle saladuse nimi, kuhu on talletatud IoT-keskuse sündmuste keskuse ühenduse string.</span><span class="sxs-lookup"><span data-stu-id="4ba15-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="4ba15-119">Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="4ba15-120">**Redis-vahemälu võtmehoidla URI** – avage võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Ülevaade** ja kopeerige väärtus **DNS-i nimi**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="4ba15-121">Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="4ba15-122">**Redis-vahemälu lõpp-punkti saladuse nimi** – avage võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Saladused** ja kopeerige selle saladuse nimi, kuhu on talletatud Redis-vahemälu ühenduse string.</span><span class="sxs-lookup"><span data-stu-id="4ba15-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="4ba15-123">Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="4ba15-124">Tingimustega nõustumiseks valige märkeruut.</span><span class="sxs-lookup"><span data-stu-id="4ba15-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="4ba15-125">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-125">Select **Install**.</span></span>
8. <span data-ttu-id="4ba15-126">Kuvatakse teateaken, mis ütleb „Lisandmoodul on installimiseks edukalt käivitatud”.</span><span class="sxs-lookup"><span data-stu-id="4ba15-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="4ba15-127">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-127">Select **OK**.</span></span>

<span data-ttu-id="4ba15-128">LCS-i seadistamine on nüüd lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="4ba15-128">LCS setup is now completed.</span></span> <span data-ttu-id="4ba15-129">Järgmine etapp on [stsenaariumide seadistamine](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="4ba15-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="4ba15-130">Lisandmooduli desinstallimine</span><span class="sxs-lookup"><span data-stu-id="4ba15-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="4ba15-131">[Keelake stsenaariumid](iot-scenario-setup.md#disable-a-scenario) Supply Chain Managementis.</span><span class="sxs-lookup"><span data-stu-id="4ba15-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#disable-a-scenario).</span></span>
2. <span data-ttu-id="4ba15-132">Avage LCS-is teenuse Supply Chain Management keskkonna üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="4ba15-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="4ba15-133">Kerige alla jaotiseni **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="4ba15-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="4ba15-134">Valige **Desinstalli** IoT iseõppimisvõime lisandmooduli jaoks.</span><span class="sxs-lookup"><span data-stu-id="4ba15-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
