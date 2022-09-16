---
title: Simuleeritud anduri seadistamine testimiseks
description: See artikkel kirjeldab, kuidas seadistada simulaator, mida saate kasutada Anduri andmeteabe testimiseks ilma ühegi füüsilise anduri installimiseta.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: edfa20bec7438124844f8b6afa91ca4941b6bb56
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428986"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>Simuleeritud anduri seadistamine testimiseks

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Kui soovite testeerida Anduri andmeinfot ilma ühegi füüsilise anduri installimiseta, *võite kasutada Windows Azure’i IoT Online Simulator* teenust, et saata need oma seadmete Interneti (IoT) lahendusele Microsoft Azure. Simulaator kohta lisateabe saamiseks vt [Connect Thephoidla Pi online simulaator Azure IoT keskusega (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="create-a-device-in-azure-iot-hub"></a>Seadme loomine Azure’i IoT keskuses

Teil tuleb kõigepealt seadistada seade, et autentida azure’i IoT keskusele signaali.

1. Azure’is minge nende ressursigrupi ressursside loendisse, mille lõite kasutuseks Koos Anduri andmeteabega. (Lisateavet vt teemast [Juurutage IoT-lahendus Azure’is](sdi-deploy-iot-solution-on-azure.md).)
1. Ressursiloendist leidke kirje, kus väli **Tüüp on** seadistatud *IoT keskusele*. **Valige veerus** Nimi nimi ressursi üksikasjade lehe avamiseks.
1. Valige vasakul navigeerimispaanil **Seadmed**.
1. Lehel Seadmed **valige** lisa **seade**.
1. **Seadke lehel Seadme** loomine järgmised väljad:

    - **Seadme ID** : sisestage uue seadme nimi (nt *Minu-IoT-seade*).
    - **Autentimise tüüp** – valige *sümmeetrilised võtmed*.
    - **Võtmete automaatne loomine** – märkige see ruut.
    - **Ühenda seade IoT keskusega –** valige *luba*.

1. Valige **salvestamine**, et naasta lehele **Seadmed**.
1. Otsige loendist uus seade. **Veerus Seadme ID** valige nimi, et avada seadme üksikasjade leht. Kui te ei näe loendis uut seadet, värskendage lehekülge.
1. Kopeerige **esmase ühenduse stringi** väärtus (näiteks klõpsates nuppu Kopeeri **lõikelauale**). Seda väärtust vajate hiljem, kui seadistate Jada Pi IoT simulaator simulatsiooni loomiseks. Seetõttu kaaluge selle kleepimist praegu tekstifailiks.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>Azure’i ühendusstringi lisaminePakkumiste Pi IoT simulaatorile

Järgige neid samme, et lisada ühendusstring seadmest Azure IoT keskuses skripte skriptidesse klienditeeninduse teenuses.

1. Saate avadaPakkumiste [Pi IoT simulaatori](https://azure-samples.github.io/raspberry-pi-web-simulator/).
1. Koodiredaktori paanil otsige rida, mis sisaldab järgmist käsku.

    `const connectionString = '[Your IoT hub device connection string]';`

1. Asendage spikritekst (k.a sulgud) **primaarse ühendusstringi** väärtusega, mille kopeerisite eelmisesse jaotisesse. Tulemus peals sarnanema järgmise näitega.

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>Anduri ID-de ja väärtuste lisamine töökoormusele Tomapi IoT simulaatoris

Nüüd peate seadistamaSimulatsiooni Pi IoT simuleeritud andrite ja väärtustega, mida need saadavad lisakoormustena.

- Vastavalt järgmise koodi koodile leidke Ja redigeerige Seda Ning redigeerige Selle `getMessage` kood redaktori abil, et see vastaks järgmistele koodidele. (Andurid seadistatakse ridadel `cb()` .)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > Sisestamismootori ID-d, mis on koodiredaktoris määratud Sisestamispi IoT simulaatori jaoks, peavad olema identsed toorkoodidega, mille määratlete tarneahela halduse stsenaariumite puhul hiljem. Eelnevas näites kasutatud kood kasutab inimese loetavat anduri ID-d. Kuid tegelikus stsenaariumis on anduri ID-d globaalselt kordumatu ID-d (GUID) väärtused, mille annab andja tootja. Selles näites kasutatud inimesele loetavaid anduri ID-sid kasutatakse ka toote kvaliteedi stsenaariumi, vara hoolduse stsenaariumi, [...](sdi-scenario-product-quality.md)[...](sdi-scenario-asset-maintenance.md)[tootmise viivituste stsenaariumi ja masina oleku stsenaariumi näidetes.](sdi-scenario-production-delays.md)[...](sdi-scenario-equipment-downtime.md) Seetõttu kasutage seda koodi, kui töötate läbi nende stsenaariumite.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>Anduri signaalide saatmise intervalli redigeerimine

Nüüd peate seadistama intervalli, mille järel Sisestab Sisestaja Pi IoT simulaator sõnumeid teleksisõnumitele.

1. Simulatsiooni Sisestamis pi IoT koodiredaktoris leidke järgmine funktsioon kutsumiseks.

    `setInterval(sendMessage, 2000);`

2. Vaikimisi saadab Millisep installimis pi IoT simulaator igal 2000 millisekundi kohta signaali (kaks sekundit). Saate väärtust korrigeerida vastavalt vajadusele.

## <a name="run-the-raspberry-pi-iot-simulator"></a>Run the Simulator Pi IoT simulaator

- Simuleeritud **seadmega** simuleeritud andmete saatmiseks klõpsake simulaatori käivitamiseks nuppu Käivita.
