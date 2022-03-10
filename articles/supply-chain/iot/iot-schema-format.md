---
title: IoT Hub sõnumite skeemivormingud
description: See teema selgitab, kuidas peaksite kujundama sõnumiskeemi, mida saate kasutada IoT-Intelligence`s.
author: tonyafehr
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b24a6e14182baa91299abad0da2987b2dca92601
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781608"
---
# <a name="schema-formats-for-iot-hub-messages"></a>IoT Hub sõnumite skeemivormingud

[!include [banner](../../includes/banner.md)]

See teema selgitab, kuidas peaksite kujundama sõnumiskeemi, mida saate kasutada IoT-Intelligence`s.

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