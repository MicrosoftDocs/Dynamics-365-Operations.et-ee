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
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 15021281b9ec33cd0552bca16e3054d0d3cdd589
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803061"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="5f26c-103">IoT iseõppimisvõime jälgimine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="5f26c-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f26c-104">Selles teemas selgitatakse, kuidas jälgida ja hallata IoT iseõppimisvõimet.</span><span class="sxs-lookup"><span data-stu-id="5f26c-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="5f26c-105">Stsenaariumide jälgimine Microsoft Dynamics 365 Supply Chain Managementis</span><span class="sxs-lookup"><span data-stu-id="5f26c-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="5f26c-106">IoT iseõppimisvõime töötlemist saate jälgida mitmest kohast.</span><span class="sxs-lookup"><span data-stu-id="5f26c-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="5f26c-107">**Moodulid \> Tootmise juhtimine \> Päringud ja aruanded \> IoT iseõppimisvõime \> Teatised** – saate kuvada lahendamata teatiste loendi.</span><span class="sxs-lookup"><span data-stu-id="5f26c-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="5f26c-108">**Moodulid \> Tootmise juhtimine \> Päringud ja aruanded \> IoT iseõppimisvõime \> Suletud teatised** – saate kuvada lahendatud või lõpetatud teatiste loendi.</span><span class="sxs-lookup"><span data-stu-id="5f26c-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="5f26c-109">**Moodulid \> Tootmise juhtimine \> Päringud ja aruanded \> IoT iseõppimisvõime \> Mõõdikuvõtmed** – saate kuvada **Ressursi oleku** kordade seeria diagrammide mõõdikuvõtmeid.</span><span class="sxs-lookup"><span data-stu-id="5f26c-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="5f26c-110">**Moodulid \> Tootmise juhtimine \> Tootmise käivitamine \> Ressursi olek** – saate jälgida kindlaid mõõdikuid dialoogiboksi **Konfigureerimine** abil.</span><span class="sxs-lookup"><span data-stu-id="5f26c-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="5f26c-111">Kui stsenaarium tuvastab erandi, kuvatakse teatis erandi üksikasjadega.</span><span class="sxs-lookup"><span data-stu-id="5f26c-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="5f26c-112">**Tööruumid \> Tootmisosakonna juhtimine \> Teatised** – saate kuvada lahendamata teatiste loendi.</span><span class="sxs-lookup"><span data-stu-id="5f26c-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="5f26c-113">Töötava IoT iseõppimisvõime stsenaariumi muutmine</span><span class="sxs-lookup"><span data-stu-id="5f26c-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="5f26c-114">Kui stsenaarium on käivitatud, saate teha järgmisi muudatusi.</span><span class="sxs-lookup"><span data-stu-id="5f26c-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="5f26c-115">Uute anduri skeemi määratluste lisamine.</span><span class="sxs-lookup"><span data-stu-id="5f26c-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="5f26c-116">Uute märguande andmete väärtuste valimine.</span><span class="sxs-lookup"><span data-stu-id="5f26c-116">Select new signal data values.</span></span>
+ <span data-ttu-id="5f26c-117">Olemasolevate märguande andmete väärtuste valiku tühistamine.</span><span class="sxs-lookup"><span data-stu-id="5f26c-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="5f26c-118">Uute märguande andmete lisamine ja vastendamine.</span><span class="sxs-lookup"><span data-stu-id="5f26c-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="5f26c-119">Läve väärtuste värskendamine.</span><span class="sxs-lookup"><span data-stu-id="5f26c-119">Update threshold values.</span></span>

<span data-ttu-id="5f26c-120">Kui stsenaarium on käivitatud, on järgmised muudatused keelatud.</span><span class="sxs-lookup"><span data-stu-id="5f26c-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="5f26c-121">Mis tahes skeemi määratluste kustutamine või muutmine, mida kasutatab praegu lubatud stsenaarium.</span><span class="sxs-lookup"><span data-stu-id="5f26c-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="5f26c-122">Lubatud stsenaariumi valitud skeemi teede muutmine.</span><span class="sxs-lookup"><span data-stu-id="5f26c-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="5f26c-123">Simulatsiooni suvandid</span><span class="sxs-lookup"><span data-stu-id="5f26c-123">Simulation options</span></span>

<span data-ttu-id="5f26c-124">Saate simuleerida tehase masina signaale.</span><span class="sxs-lookup"><span data-stu-id="5f26c-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="5f26c-125">Vaadake lisateavet järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="5f26c-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="5f26c-126">IoT DevKit AZ3166 ühendamine Azure IoT Hubiga</span><span class="sxs-lookup"><span data-stu-id="5f26c-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="5f26c-127">Vaarika Pi veebisimulaatori ühendamine Azure IoT Hubiga (Node.js)</span><span class="sxs-lookup"><span data-stu-id="5f26c-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="5f26c-128">Seadme simulatsiooni lahenduse kiirendi ülevaade</span><span class="sxs-lookup"><span data-stu-id="5f26c-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
