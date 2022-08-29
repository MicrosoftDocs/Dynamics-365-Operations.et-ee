---
title: IoT iseõppimisvõime jälgimine ja haldamine
description: See artikkel selgitab, kuidas jälgida ja hallata IoT-teavet.
author: johanhoffmann
ms.date: 08/04/2022
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
ms.openlocfilehash: f1804e8b9cfa407f6549dc146df17338c4d51572
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228855"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT iseõppimisvõime jälgimine ja haldamine

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

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
