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
ms.openlocfilehash: ae6b36c40d2f2f9e5266dfb3e2d1cbbb57755222
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803087"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>IoT iseõppimisvõime lisandmooduli installimine LCS-is

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas installida IoT iseõppimisvõime lisandmoodulit teenuses Microsoft Dynamics Lifecycle Services (LCS). Pange tähele, et lisandmooduleid ei saa installida demo/prooviversiooni keskkonnas. Enne lisandmooduli installimist peate [looma Azure'i ressursid](iot-azure-setup.md).

## <a name="set-up-the-lcs-environment"></a>LCS-i keskkonna seadistamine

1. Avage LCS ja minge oma Microsoft Dynamics 365 Supply Chain Managementi keskkonda.
2. Kerige alla jaotiseni **Keskkonna lisandmoodulid**.
3. Valige **Installi uus lisandmoodul**, et kuvada selle keskkonna jaoks lubatud lisandmoodulite loend.
4. Valige dialoogiboksis **Installitava lisandmooduli valimine** suvand **IoT iseõppimisvõime**.
5. Sisestage dialoogiboksis **Seadistuse lisandmoodul** oma IoT-keskuse ja Redis-vahemälu üksikasjad. Nõutavad väärtused leiate võtmehoidlast, mille lõite jaotises [Azure'i ressursside loomine](iot-azure-setup.md).

    + **Rentniku ID** – avage Azure'i portaali võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Ülevaade** ja kopeerige väärtus **Kausta ID**. Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.
    + **IoT sündmuste keskusega ühilduv lõpp-punkti võtmehoidla URI** – avage võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Ülevaade** ja kopeerige väärtus **DNS-i nimi**. Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.
    + **IoT sündmuste keskusega ühilduv lõpp-punkti saladuse nimi** – avage võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Saladused** ja kopeerige selle saladuse nimi, kuhu on talletatud IoT-keskuse sündmuste keskuse ühenduse string. Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.
    + **Redis-vahemälu võtmehoidla URI** – avage võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Ülevaade** ja kopeerige väärtus **DNS-i nimi**. Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.
    + **Redis-vahemälu lõpp-punkti saladuse nimi** – avage võtmehoidla ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Saladused** ja kopeerige selle saladuse nimi, kuhu on talletatud Redis-vahemälu ühenduse string. Kleepige see väärtus dialoogiboksi **Seadistuse lisandmoodul**.

6. Tingimustega nõustumiseks valige märkeruut.
7. Valige **Installi**.
8. Kuvatakse teateaken, mis ütleb „Lisandmoodul on installimiseks edukalt käivitatud”. Valige nupp **OK**.

LCS-i seadistamine on nüüd lõpule viidud. Järgmine etapp on [stsenaariumide seadistamine](iot-scenario-setup.md).

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>Lisandmooduli desinstallimine

1. [Keelake stsenaariumid](iot-scenario-setup.md#how-to-disable-a-scenario) Supply Chain Managementis.
2. Avage LCS-is teenuse Supply Chain Management keskkonna üksikasjad.
3. Kerige alla jaotiseni **Keskkonna lisandmoodulid**.
4. Valige **Desinstalli** IoT iseõppimisvõime lisandmooduli jaoks.
