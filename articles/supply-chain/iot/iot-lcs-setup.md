---
title: IoT iseõppimisvõime lisandmooduli installimine LCS-is
description: Selles teemas selgitatakse, kuidas installida IoT iseõppimisvõime lisandmoodulit teenuses Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386505"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="cb613-103">IoT iseõppimisvõime lisandmooduli installimine LCS-is</span><span class="sxs-lookup"><span data-stu-id="cb613-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb613-104">Selles teemas selgitatakse, kuidas installida IoT iseõppimisvõime lisandmoodulit teenuses Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="cb613-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="cb613-105">Enne lisandmooduli installimist peate [looma Azure'i ressursid](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="cb613-105">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="cb613-106">LCS-i keskkonna seadistamine</span><span class="sxs-lookup"><span data-stu-id="cb613-106">Set up the LCS environment</span></span>

1. <span data-ttu-id="cb613-107">Avage LCS ja minge oma Microsoft Dynamics 365 Supply Chain Managementi keskkonda.</span><span class="sxs-lookup"><span data-stu-id="cb613-107">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="cb613-108">Kerige alla jaotiseni **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="cb613-108">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="cb613-109">Valige **Installi uus lisandmoodul**, et kuvada selle keskkonna jaoks lubatud lisandmoodulite loend.</span><span class="sxs-lookup"><span data-stu-id="cb613-109">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="cb613-110">Valige dialoogiboksis **Installitava lisandmooduli valimine** suvand **IoT iseõppimisvõime**.</span><span class="sxs-lookup"><span data-stu-id="cb613-110">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="cb613-111">Sisestage dialoogiboksis **Seadistuse lisandmoodul** oma IoT-keskuse ja Redis-vahemälu üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="cb613-111">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="cb613-112">Nõutavad väärtused leiate võtmehoidlast, mille lõite jaotises [Azure'i ressursside loomine](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="cb613-112">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="cb613-113">**Rentniku ID** – avage Azure'i portaali võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Ülevaade** ja kopeerige väärtus **Kausta ID**.</span><span class="sxs-lookup"><span data-stu-id="cb613-113">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="cb613-114">Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="cb613-114">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="cb613-115">**IoT sündmuste keskusega ühilduv lõpp-punkti võtmehoidla URI** – avage võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Ülevaade** ja kopeerige väärtus **DNS-i nimi**.</span><span class="sxs-lookup"><span data-stu-id="cb613-115">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="cb613-116">Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="cb613-116">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="cb613-117">**IoT sündmuste keskusega ühilduv lõpp-punkti saladuse nimi** – avage võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Saladused** ja kopeerige selle saladuse nimi, kuhu on talletatud IoT-keskuse sündmuste keskuse ühenduse string.</span><span class="sxs-lookup"><span data-stu-id="cb613-117">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="cb613-118">Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="cb613-118">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="cb613-119">**Redis-vahemälu võtmehoidla URI** – avage võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Ülevaade** ja kopeerige väärtus **DNS-i nimi**.</span><span class="sxs-lookup"><span data-stu-id="cb613-119">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="cb613-120">Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="cb613-120">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="cb613-121">**Redis-vahemälu lõpp-punkti saladuse nimi** – avage võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Saladused** ja kopeerige selle saladuse nimi, kuhu on talletatud Redis-vahemälu ühenduse string.</span><span class="sxs-lookup"><span data-stu-id="cb613-121">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="cb613-122">Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="cb613-122">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="cb613-123">Tingimustega nõustumiseks valige märkeruut.</span><span class="sxs-lookup"><span data-stu-id="cb613-123">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="cb613-124">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="cb613-124">Select **Install**.</span></span>
8. <span data-ttu-id="cb613-125">Kuvatakse teateaken, mis ütleb „Lisandmoodul on installimiseks edukalt käivitatud”.</span><span class="sxs-lookup"><span data-stu-id="cb613-125">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="cb613-126">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="cb613-126">Select **OK**.</span></span>

<span data-ttu-id="cb613-127">LCS-i seadistamine on nüüd lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="cb613-127">LCS setup is now completed.</span></span> <span data-ttu-id="cb613-128">Järgmine etapp on [stsenaariumide seadistamine](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="cb613-128">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="cb613-129">Lisandmooduli desinstallimine</span><span class="sxs-lookup"><span data-stu-id="cb613-129">Uninstall the add-in</span></span>

1. <span data-ttu-id="cb613-130">[Keelake stsenaariumid](iot-scenario-setup.md#how-to-disable-a-scenario) Supply Chain Managementis.</span><span class="sxs-lookup"><span data-stu-id="cb613-130">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="cb613-131">Avage LCS-is teenuse Supply Chain Management keskkonna üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="cb613-131">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="cb613-132">Kerige alla jaotiseni **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="cb613-132">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="cb613-133">Valige **Desinstalli** IoT iseõppimisvõime lisandmooduli jaoks.</span><span class="sxs-lookup"><span data-stu-id="cb613-133">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
