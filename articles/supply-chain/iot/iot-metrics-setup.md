---
title: IoT iseõppimise mõõdikute seadistamine
description: See artikkel selgitab, kuidas seadistada IoT-teabe mõõdikuid.
author: johanhoffmann
ms.date: 08/04/2022
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
ms.openlocfilehash: fddfee837761a4f23b42257424582a3c76c3d493
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228323"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>IoT iseõppimise mõõdikute seadistamine

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

## <a name="configure-metrics"></a>Konfigureerige mõõdikud

Kui soovite vaadata oma sõnumite ajaseeria diagramme, peate seadistama Microsoft Dynamics 365 Supply Chain Management mõõduread järgmiste sammude abil.

1. Redis-vahemälu ühendusstringi kopeerimine:

    1. Azure'i portaalis minge Redis-vahelehele.
    2. Avage **Sätted** \> **pääsuvõtmed**.
    3. Kopeerige väärtus väljajalt **Peamine ühenduse string**.

2. Avage rakenduses Supply Chain Management suvand **Tootmise juhtimine \> Seadistus \> IoT iseõppimine \> Stenaariumi parameetrid**.
3. **Stsenaariumi parameetrite** lehel **Ajaseeria** vahekaardil **Redis mõõdikute poe ühenduse string** kleepige varem kopeeritud ühendusstring. See samm võimaldab Azure'i IoT Hub mõõdikute visualiseerimist rakenduses Supply Chain Management. Kui kleebite väärtuse väljale, kuvatakse see kui **\*\*\*\*\*\***.

    > [!NOTE]
    > Redise vahemälu ühenduse stringi värskendamisel peate värskendama ka seda välja.

4. Minge **tootmise juhtimise \> päringud ja aruanded \> IoT iseõppimine \> mõõdikute võtmed**.
5. Valige **mõõdikute võtmete** lehel suvand **Uuenda**.
6. Pange **uuenda mõõdikute võtmed** dialoogiboksis tähele, et **taustal käitamise** väli on valitud. Valige nupp **OK**.

Kõik redis-vahemälus toodud mõõdikute võtmed tuuakse ja lisatakse **mõõdikute võtmete** loendisse. Mõõdikute väärtusi ei kuvata kuni [lubate stsenaariumid](iot-scenario-setup.md).

## <a name="configure-the-resource-status-time-series"></a>Ressursi oleku ajaseeria konfigureerimine

**Ressursi oleku** ajaseeria konfigureerimiseks järgige neid samme.

1. Rakenduses Supply Chain Management minge **tootmise juhtimine \> tootmise teostamine \> ressursi olek**.
2. Tehke lehel **Reursside olek** valik **Konfigureeri**.
2. **Konfigureerimise** dialoogiakna loendis **Ressurss** valige jälgitav üksus.
3. Valige **Redigeeri** nupp **Ajaseeriatele 1**.
4. Dialoogiboksis **Valige ajaseeria** valige ruudustikus mõõdikud. (Saate kasutada ka **Uuenda mõõdikute võtmed** linki selle dialoogiboksi mõõdikute võtmete uuendamiseks.)
5. Valige **Ok** et naasta **konfigureerimise** dialoogiboksi.
6. Sisestage kuva nimi.
7. Väljal **Näita andmevormi** väljal valige aja raam.
8. Valige nupp **OK**.

Diagramm on kuvatud.

## <a name="delete-a-metric-key"></a>Mõõdikute võtme kustutamine

1. Minge rakenduses Supply Chain Management **tootmise juhtimine \> päringud ja aruanded \> IoT iseõppimine \> mõõdikute võtmed**.
2. Valige **mõõdiku võtmete** lehel valige kustutamiseks mõõdikute võti.
3. Valige **Kustuta**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]