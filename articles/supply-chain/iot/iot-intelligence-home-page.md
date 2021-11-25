---
title: IoT iseõppimisvõime avaleht
description: See teema sisaldab linke IoT iseõppimise teabega seotult.
author: tonyafehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b6c179052cdb9d1ca808d9cba089163bde0d5d5
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782677"
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

+ **Tootmise viivitused** – see stsenaarium võrdleb tegelikku tsükli aega plaanitud tsükli ajaga. Supply Chain Management teavitab teid, kui tootmist ei ole graafikus, nii et saate tegevusefektiivsuse suurendamiseks ja tellimuse viivituste vältimiseks suhelda.
+ **Seadmete ettemaks** – see stsenaarium võrdleb mõõdetud ülesaega kasutaja määratletud parameetritega. Supply Chain Management teavitab teid, kui lävi on ületatud, nii et saate teha selliseid toiminguid, nagu tootmistellimuse uuesti plaanimine või hooldustöötellimuse loomine.
+ **Toote kvaliteet** - selle stsenaariumi puhul võrreldakse lugemisi nagu näiteks niiskuse ja temperatuuri kasutaja määratud kvaliteedi mõõdikutega. Supply Chain Management teavitab teid hälbe ilmnemisel, nii et saate vastu võtta kvaliteedistandardite säilitamiseks ja jäätmekäitluse minimeerimiseks.

Järgmine näide näitab Azure'i IoT Hub, IoT-iseõppimine ja Supply Chain Management vaheline suhtlust.

![IoT Hub, IoT iseõppimine ja Supply Chain Management.](media/iot_intelligence.png)

## <a name="setup"></a>Häälestus

Saate seadistada ja konfigureerida IoT-iseõppimise ilma koodi kirjutamata. Siin on põhietapid.

1. [Seadistage Azure'i ressursid](iot-azure-setup.md)– looge IoT keskus, Redis-vahemälu ja võtmehoidla, mida saab kasutada Supply Chain Management rakenduses.
2. [IoT keskuse teateskeemi vormingud](iot-schema-format.md) – konfigureerige seadmeid sõnumite saatmiseks IoT keskusesse ja määratlege JavaScript Object Notation (JSON) teatevorming.
3. Funktsioonihalduses lubage IoT iseõppimise funktsiooni lipp. 
4. [Installige IoT iseõppimise lisandmoodul Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – installige lisandmoodul LCS-is ja konfigureerige Azure'i saladused.
5. [Seadistage mõõdikud](iot-metrics-setup.md) – seadistage mõõdikud rakenduses Supply Chain Management.
6. [Stsenaariumi häälestus](iot-scenario-setup.md) - seadistage stsenaariumid rakenduses Supply Chain Management.

## <a name="tracking-and-maintenance"></a>Jälgimine ja hooldus

+ [Jälgi stsenaariumeid rakenduses Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
+ [Stsenaariumi keelamine](iot-scenario-setup.md#disable-a-scenario)
+ [Lisandmooduli desinstallimine](iot-lcs-setup.md#uninstall-addin)
+ [Töötava IoT iseõppimisvõime stsenaariumi muutmine](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [Simulatsiooni suvandid](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]