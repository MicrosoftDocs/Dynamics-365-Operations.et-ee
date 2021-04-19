---
title: IoT iseõppimisvõime jälgimine ja haldamine
description: Selles teemas selgitatakse, kuidas jälgida ja hallata IoT iseõppimisvõimet.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 94665b3646456b689a8e65e94b098e86e467d5e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813071"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="5f69e-103">IoT iseõppimisvõime jälgimine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="5f69e-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f69e-104">Selles teemas selgitatakse, kuidas jälgida ja hallata IoT iseõppimisvõimet.</span><span class="sxs-lookup"><span data-stu-id="5f69e-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="5f69e-105">Stsenaariumide jälgimine Microsoft Dynamics 365 Supply Chain Managementis</span><span class="sxs-lookup"><span data-stu-id="5f69e-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="5f69e-106">IoT iseõppimisvõime töötlemist saate jälgida mitmest kohast.</span><span class="sxs-lookup"><span data-stu-id="5f69e-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="5f69e-107">**Moodulid \> Tootmise juhtimine \> Päringud ja aruanded \> IoT iseõppimisvõime \> Teatised** – saate kuvada lahendamata teatiste loendi.</span><span class="sxs-lookup"><span data-stu-id="5f69e-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="5f69e-108">**Moodulid \> Tootmise juhtimine \> Päringud ja aruanded \> IoT iseõppimisvõime \> Suletud teatised** – saate kuvada lahendatud või lõpetatud teatiste loendi.</span><span class="sxs-lookup"><span data-stu-id="5f69e-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="5f69e-109">**Moodulid \> Tootmise juhtimine \> Päringud ja aruanded \> IoT iseõppimisvõime \> Mõõdikuvõtmed** – saate kuvada **Ressursi oleku** kordade seeria diagrammide mõõdikuvõtmeid.</span><span class="sxs-lookup"><span data-stu-id="5f69e-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="5f69e-110">**Moodulid \> Tootmise juhtimine \> Tootmise käivitamine \> Ressursi olek** – saate jälgida kindlaid mõõdikuid dialoogiboksi **Konfigureerimine** abil.</span><span class="sxs-lookup"><span data-stu-id="5f69e-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="5f69e-111">Kui stsenaarium tuvastab erandi, kuvatakse teatis erandi üksikasjadega.</span><span class="sxs-lookup"><span data-stu-id="5f69e-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="5f69e-112">**Tööruumid \> Tootmisosakonna juhtimine \> Teatised** – saate kuvada lahendamata teatiste loendi.</span><span class="sxs-lookup"><span data-stu-id="5f69e-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="5f69e-113">Töötava IoT iseõppimisvõime stsenaariumi muutmine</span><span class="sxs-lookup"><span data-stu-id="5f69e-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="5f69e-114">Kui stsenaarium on käivitatud, saate teha järgmisi muudatusi.</span><span class="sxs-lookup"><span data-stu-id="5f69e-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="5f69e-115">Uute anduri skeemi määratluste lisamine.</span><span class="sxs-lookup"><span data-stu-id="5f69e-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="5f69e-116">Uute märguande andmete väärtuste valimine.</span><span class="sxs-lookup"><span data-stu-id="5f69e-116">Select new signal data values.</span></span>
+ <span data-ttu-id="5f69e-117">Olemasolevate märguande andmete väärtuste valiku tühistamine.</span><span class="sxs-lookup"><span data-stu-id="5f69e-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="5f69e-118">Uute märguande andmete lisamine ja vastendamine.</span><span class="sxs-lookup"><span data-stu-id="5f69e-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="5f69e-119">Läve väärtuste värskendamine.</span><span class="sxs-lookup"><span data-stu-id="5f69e-119">Update threshold values.</span></span>

<span data-ttu-id="5f69e-120">Kui stsenaarium on käivitatud, on järgmised muudatused keelatud.</span><span class="sxs-lookup"><span data-stu-id="5f69e-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="5f69e-121">Mis tahes skeemi määratluste kustutamine või muutmine, mida kasutatab praegu lubatud stsenaarium.</span><span class="sxs-lookup"><span data-stu-id="5f69e-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="5f69e-122">Lubatud stsenaariumi valitud skeemi teede muutmine.</span><span class="sxs-lookup"><span data-stu-id="5f69e-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="5f69e-123">Simulatsiooni suvandid</span><span class="sxs-lookup"><span data-stu-id="5f69e-123">Simulation options</span></span>

<span data-ttu-id="5f69e-124">Saate simuleerida tehase masina signaale.</span><span class="sxs-lookup"><span data-stu-id="5f69e-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="5f69e-125">Vaadake lisateavet järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="5f69e-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="5f69e-126">IoT DevKit AZ3166 ühendamine Azure IoT Hubiga</span><span class="sxs-lookup"><span data-stu-id="5f69e-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="5f69e-127">Vaarika Pi veebisimulaatori ühendamine Azure IoT Hubiga (Node.js)</span><span class="sxs-lookup"><span data-stu-id="5f69e-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="5f69e-128">Seadme simulatsiooni lahenduse kiirendi ülevaade</span><span class="sxs-lookup"><span data-stu-id="5f69e-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]