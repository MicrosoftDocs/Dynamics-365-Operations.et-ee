---
title: IoT iseõppimisvõime avaleht
description: See teema sisaldab linke IoT iseõppimise teabega seotult.
author: johanhoffmann
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2386d71fde8196304fde846cbff4cd45d1edc834
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674417"
---
# <a name="iot-intelligence-home-page"></a>IoT iseõppimisvõime avaleht

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> See funktsioon on praegu saadaval ainult järgmistes riikides/regioonides:
>
> - USA (Ameerika Ühendriigid)
> - EL (Euroopa Liit)
> - AU (Austraalia)
> - Ca (Kanada)
> - UK (Ühendkuningriik)

IoT iseõppimine on Microsoft Dynamics 365 Supply Chain Management lisandmoodul. See integreerib asjade internetti (IoT) signaalid Supply Chain Management andmetega, et luua tegevusülevaateid.

IoT iseõppimine toetab järgmisi stsenaariume:

- **Tootmise viivitused** – see stsenaarium võrdleb tegelikku tsükli aega plaanitud tsükli ajaga. Supply Chain Management teavitab teid, kui tootmist ei ole graafikus, nii et saate tegevusefektiivsuse suurendamiseks ja tellimuse viivituste vältimiseks suhelda.
- **Seadmete ettemaks** – see stsenaarium võrdleb mõõdetud ülesaega kasutaja määratletud parameetritega. Supply Chain Management teavitab teid, kui lävi on ületatud, nii et saate teha selliseid toiminguid, nagu tootmistellimuse uuesti plaanimine või hooldustöötellimuse loomine.
- **Toote kvaliteet** - selle stsenaariumi puhul võrreldakse lugemisi nagu näiteks niiskuse ja temperatuuri kasutaja määratud kvaliteedi mõõdikutega. Supply Chain Management teavitab teid hälbe ilmnemisel, nii et saate vastu võtta kvaliteedistandardite säilitamiseks ja jäätmekäitluse minimeerimiseks.

Järgmine näide näitab Azure'i IoT Hub, IoT-iseõppimine ja Supply Chain Management vaheline suhtlust.

![IoT Hub, IoT iseõppimine ja Supply Chain Management.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>Jälgimine ja hooldus

- [Jälgi stsenaariumeid rakenduses Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
- [Stsenaariumi keelamine](iot-scenario-setup.md#disable-a-scenario)
- [Töötava IoT iseõppimisvõime stsenaariumi muutmine](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [Simulatsiooni suvandid](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]