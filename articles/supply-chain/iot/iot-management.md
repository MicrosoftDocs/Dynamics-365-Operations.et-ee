---
title: IoT iseõppimisvõime jälgimine ja haldamine
description: Selles teemas selgitatakse, kuidas jälgida ja hallata IoT iseõppimisvõimet.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7082f9e7640e8ef1b2873a954327b61a440e8ad0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000002"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="7eed1-103">IoT iseõppimisvõime jälgimine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="7eed1-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7eed1-104">Selles teemas selgitatakse, kuidas jälgida ja hallata IoT iseõppimisvõimet.</span><span class="sxs-lookup"><span data-stu-id="7eed1-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="7eed1-105">Stsenaariumide jälgimine Microsoft Dynamics 365 Supply Chain Managementis</span><span class="sxs-lookup"><span data-stu-id="7eed1-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="7eed1-106">IoT iseõppimisvõime töötlemist saate jälgida mitmest kohast.</span><span class="sxs-lookup"><span data-stu-id="7eed1-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="7eed1-107">**Moodulid \> Tootmise juhtimine \> Päringud ja aruanded \> IoT iseõppimisvõime \> Teatised** – saate kuvada lahendamata teatiste loendi.</span><span class="sxs-lookup"><span data-stu-id="7eed1-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="7eed1-108">**Moodulid \> Tootmise juhtimine \> Päringud ja aruanded \> IoT iseõppimisvõime \> Suletud teatised** – saate kuvada lahendatud või lõpetatud teatiste loendi.</span><span class="sxs-lookup"><span data-stu-id="7eed1-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="7eed1-109">**Moodulid \> Tootmise juhtimine \> Päringud ja aruanded \> IoT iseõppimisvõime \> Mõõdikuvõtmed** – saate kuvada **Ressursi oleku** kordade seeria diagrammide mõõdikuvõtmeid.</span><span class="sxs-lookup"><span data-stu-id="7eed1-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="7eed1-110">**Moodulid \> Tootmise juhtimine \> Tootmise käivitamine \> Ressursi olek** – saate jälgida kindlaid mõõdikuid dialoogiboksi **Konfigureerimine** abil.</span><span class="sxs-lookup"><span data-stu-id="7eed1-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="7eed1-111">Kui stsenaarium tuvastab erandi, kuvatakse teatis erandi üksikasjadega.</span><span class="sxs-lookup"><span data-stu-id="7eed1-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="7eed1-112">**Tööruumid \> Tootmisosakonna juhtimine \> Teatised** – saate kuvada lahendamata teatiste loendi.</span><span class="sxs-lookup"><span data-stu-id="7eed1-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="7eed1-113">Töötava IoT iseõppimisvõime stsenaariumi muutmine</span><span class="sxs-lookup"><span data-stu-id="7eed1-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="7eed1-114">Kui stsenaarium on käivitatud, saate teha järgmisi muudatusi.</span><span class="sxs-lookup"><span data-stu-id="7eed1-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="7eed1-115">Uute anduri skeemi määratluste lisamine.</span><span class="sxs-lookup"><span data-stu-id="7eed1-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="7eed1-116">Uute märguande andmete väärtuste valimine.</span><span class="sxs-lookup"><span data-stu-id="7eed1-116">Select new signal data values.</span></span>
+ <span data-ttu-id="7eed1-117">Olemasolevate märguande andmete väärtuste valiku tühistamine.</span><span class="sxs-lookup"><span data-stu-id="7eed1-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="7eed1-118">Uute märguande andmete lisamine ja vastendamine.</span><span class="sxs-lookup"><span data-stu-id="7eed1-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="7eed1-119">Läve väärtuste värskendamine.</span><span class="sxs-lookup"><span data-stu-id="7eed1-119">Update threshold values.</span></span>

<span data-ttu-id="7eed1-120">Kui stsenaarium on käivitatud, on järgmised muudatused keelatud.</span><span class="sxs-lookup"><span data-stu-id="7eed1-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="7eed1-121">Mis tahes skeemi määratluste kustutamine või muutmine, mida kasutatab praegu lubatud stsenaarium.</span><span class="sxs-lookup"><span data-stu-id="7eed1-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="7eed1-122">Lubatud stsenaariumi valitud skeemi teede muutmine.</span><span class="sxs-lookup"><span data-stu-id="7eed1-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="7eed1-123">Simulatsiooni suvandid</span><span class="sxs-lookup"><span data-stu-id="7eed1-123">Simulation options</span></span>

<span data-ttu-id="7eed1-124">Saate simuleerida tehase masina signaale.</span><span class="sxs-lookup"><span data-stu-id="7eed1-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="7eed1-125">Vaadake lisateavet järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="7eed1-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="7eed1-126">IoT DevKit AZ3166 ühendamine Azure IoT Hubiga</span><span class="sxs-lookup"><span data-stu-id="7eed1-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="7eed1-127">Vaarika Pi veebisimulaatori ühendamine Azure IoT Hubiga (Node.js)</span><span class="sxs-lookup"><span data-stu-id="7eed1-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="7eed1-128">Seadme simulatsiooni lahenduse kiirendi ülevaade</span><span class="sxs-lookup"><span data-stu-id="7eed1-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
