---
title: IoT iseõppimisvõime jälgimine ja haldamine
description: See artikkel selgitab, kuidas jälgida ja hallata IoT-teavet.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a640b523adac619377e19d670f932d4d85cfb6a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852414"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT iseõppimisvõime jälgimine ja haldamine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas jälgida ja hallata IoT-teavet.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Stsenaariumide jälgimine Microsoft Dynamics 365 Supply Chain Managementis

IoT iseõppimisvõime töötlemist saate jälgida mitmest kohast.

+ **Moodulid \> Tootmise juhtimine \> Päringud ja aruanded \> IoT iseõppimisvõime \> Teatised** – saate kuvada lahendamata teatiste loendi.
+ **Moodulid \> Tootmise juhtimine \> Päringud ja aruanded \> IoT iseõppimisvõime \> Suletud teatised** – saate kuvada lahendatud või lõpetatud teatiste loendi.
+ **Moodulid \> Tootmise juhtimine \> Päringud ja aruanded \> IoT iseõppimisvõime \> Mõõdikuvõtmed** – saate kuvada **Ressursi oleku** kordade seeria diagrammide mõõdikuvõtmeid.
+ **Moodulid \> Tootmise juhtimine \> Tootmise käivitamine \> Ressursi olek** – saate jälgida kindlaid mõõdikuid dialoogiboksi **Konfigureerimine** abil. Kui stsenaarium tuvastab erandi, kuvatakse teatis erandi üksikasjadega.
+ **Tööruumid \> Tootmisosakonna juhtimine \> Teatised** – saate kuvada lahendamata teatiste loendi.

## <a name="modify-a-running-iot-intelligence-scenario"></a>Töötava IoT iseõppimisvõime stsenaariumi muutmine

Kui stsenaarium on käivitatud, saate teha järgmisi muudatusi.

+ Uute anduri skeemi määratluste lisamine.
+ Uute märguande andmete väärtuste valimine.
+ Olemasolevate märguande andmete väärtuste valiku tühistamine.
+ Uute märguande andmete lisamine ja vastendamine.
+ Läve väärtuste värskendamine.

Kui stsenaarium on käivitatud, on järgmised muudatused keelatud.

+ Mis tahes skeemi määratluste kustutamine või muutmine, mida kasutatab praegu lubatud stsenaarium.
+ Lubatud stsenaariumi valitud skeemi teede muutmine.

## <a name="simulation-options"></a>Simulatsiooni suvandid

Saate simuleerida tehase masina signaale. Lisateavet vt neist artiklitest:

+ [IoT DevKit AZ3166 ühendamine Azure IoT Hubiga](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Vaarika Pi veebisimulaatori ühendamine Azure IoT Hubiga (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
