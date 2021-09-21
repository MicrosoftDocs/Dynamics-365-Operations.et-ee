---
title: Toote konfiguratsioonimudeli arvutustes ümardati valesti täisarvud
description: Täisarvu atribuudid ümardatakse valesti, kui toote konfiguratsiooni mudelid on arvutatud. Lahendage probleem lisatud kümnendkoha atribuudi ja arvutusega.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476139"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Täisarvu atribuudid ümardatakse valesti, kui toote konfiguratsiooni mudelid on arvutatud

## <a name="symptoms"></a>Sümptomid

See probleem võib ilmneda, kui sooritate järgmise seeria tegevusi:

1. Seadistage järgmised atribuudid tootmise konfiguratsiooni mudelis:

    - Sisestus (täisarv)
    - Protsent (kümnendarv)
    - Tulemus (täisarv)

2. Looge järgmiste sätetega kalkulatsioon:

    *Tulemus* = *sisend* × *protsent* ÷ 100

Sel juhul ei ümardata täisarvu tulemust alati õigesti. Kui sisend on näiteks 1000 ja protsent on 2,40, siis eeldate, et täisarvu tulemus on 24, sest 2,40 protsenti 1000-st on 24 (kümnendvormil 24,00). Selle asemel kuvatakse tulemus 23. Kuid kui protsent on 2,39, ümardatakse arvutus 24 asemel 23-ni. Kui protsent on 2,50, ümardatakse arvutus 25-ni, nagu oodatud.

## <a name="cause"></a>Põhjus

See probleem ilmneb seetõttu, et Microsoft Solver Foundation esindab sisemiselt numbreid, kasutades fraktsioone. Eelmise näite puhul on arvutuse tulemus, mille protsent on 2,40: 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375. Kui .NET annab selle väärtuse täisarvuna, tagastatakse see kui 23.

## <a name="resolution"></a>Lahendus

Seda käitumist ei muudeta, kuna teised stsenaariumid sõltuvad sellest. Eelneva näite puhul saate probleemi lahendada, kehtestades täiendava kümnendkoha atribuudi ja arvutuse.

Näiteks saate seadistada järgmised atribuudid tootmise konfiguratsiooni mudelis:

- Sisestus (täisarv)
- Protsent (kümnendarv)
- ResultDecimal (kümnendarv)
- ResultInteger (täisarv)

Seejärel saate lisada järgmisi arvutusi:

- *ResultDecimal* = *sisend* × *protsent* ÷ 100
- *ResultInteger* = *ResultDecimal*
