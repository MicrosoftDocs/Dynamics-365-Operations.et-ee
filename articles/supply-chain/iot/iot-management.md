---
title: IoT iseõppimisvõime jälgimine ja haldamine
description: Selles teemas selgitatakse, kuidas jälgida ja hallata IoT iseõppimisvõimet.
author: tonyafehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7aec17a6355caa133a671a242056e77b7f6bb461
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509552"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT iseõppimisvõime jälgimine ja haldamine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas jälgida ja hallata IoT iseõppimisvõimet.

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

Saate simuleerida tehase masina signaale. Vaadake lisateavet järgmistest teemadest.

+ [IoT DevKit AZ3166 ühendamine Azure IoT Hubiga](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Vaarika Pi veebisimulaatori ühendamine Azure IoT Hubiga (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
