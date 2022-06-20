---
title: IoT Hub sõnumite skeemivormingud
description: See artikkel selgitab, kuidas te peaksite kujundama teateskeemi, mida saate kasutada IoT-teabes.
author: johanhoffmann
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 705a2150042f9b65f1f4528d6f2699f7306996f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887453"
---
# <a name="schema-formats-for-iot-hub-messages"></a>IoT Hub sõnumite skeemivormingud

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas te peaksite kujundama teateskeemi, mida saate kasutada IoT-teabes.

## <a name="message-requirements"></a>Sõnumi nõuded

Järgmised reeglid kehtivad IoT-Intellicense teadete jälgimisel:

+ Teateskeemid peavad olema JavaScript Object Notation (JSON) vormingus.
+ UNIX **ajatempli** valikud, mille väärtust väljendatakse millisekundites (ms), peavad olema Microsoft Azure IoT Hub sõnumis.
+ Teadet jälgitakse ainult siis, kui see sisaldab kõiki stsenaariumi seadistuses määratletud atribuute. Näiteks kui määratlete **id**, **ajatempli** ja **väärtuse** atribuudid, jälgitakse järgmist teadet.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    Seda teadet ei jälgita, kuna **väärtuse** atribuut puudub.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ IoT iseõppimine ignoreerib atribuute sõnumis, mis pole stsenaariumi konfiguratsioonis määratletud. Näiteks kui määratlete **id**, **ajatempli** ja **väärtuse** atribuudid, IoT iseõppimine jälgib kõiki järgmisi teateid.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ IoT iseõppimine ignoreerib vaikselt teateid, mis ei vasta stsenaariumi konfiguratsioonikriteeriumitele.
+ Saate määratleda ja kasutada erinevat tüüpi teateskeeme.
+ Mitte igat tüüpi teateskeem ei tohi olla määratletud. Määratleda tuleb ainult skeemid, mida kasutatakse IoT iseõppimise stsenaariumite jaoks.

## <a name="id-value-pair-schema"></a>Id-väärtuse paari skeem

Id-väärtuse paar on IoT iseõppimise skeemide ühine muster. Id-väärtuspaari kasutades tagate, et teateskeem on kõigis stsenaariumites sama. Siin kuvatakse näiteks teade **seadmete ettemaksmise** või **tootmise viivituste** stsenaariumi kohta.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

Siin on **toote kvaliteedi** stsenaariumi teade.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

Mõlemad eelnevad teated sisaldavad **id** ja **väärtuse** atribuute. **Id** väärtused saab stsenaariumi häälestamise ajal vastendada **signaaliandmete väärtuste** tabelis. **Seadme ettetunnitöö** stsenaariumi korral vastendate **IoTInt.Masin1225.PartOut** väärtuse. **Toote kvaliteedi** stsenaariumi korral vastendate **IoTInt.Machine1225.Temperatuur** väärtuse.

Lisateabe saamiseks vt [Azure IoT Hub dokumentatsioon](/azure/iot-hub/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]