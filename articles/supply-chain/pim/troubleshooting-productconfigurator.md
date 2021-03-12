---
title: Tootekonfiguratsioonii tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada tootekonfiguratsioonidega töötamisel tekkivaid probleeme.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e6cfeb6a2b4166dfa9a5a5cc1b7d3d913b865ce2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999602"
---
# <a name="troubleshoot-the-product-configurator"></a>Tootekonfiguratsioonii tõrkeotsing

Selles teemas kirjeldatakse, kuidas lahendada tootekonfiguratsiooniga töötamisel tekkivaid probleeme.

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>Kauba tekst kirjutatakse üle, kui konfigureerin toote müügitellimuse real.

### <a name="issue-description"></a>Probleemi kirjeldus

See probleem ilmneb, kui loote müügitellimuse rea seadistatavale kaubale ja seejärel muudate kauba teksti. Kui konfigureerite kauba ja seejärel valite **OK**, kirjutatakse tekst üle standardse tekstiga.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on oodatud. Tekstiväli sisaldab variandi nime, mis on täidetud ainult pärast rea konfigureerimist. Seetõttu peate muutma teksti pärast rea konfigureerimist, mitte varem.

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Täisarvu atribuudid ümardatakse valesti, kui toote konfiguratsiooni mudelid on arvutatud.

### <a name="issue-description"></a>Probleemi kirjeldus

See probleem võib ilmneda, kui sooritate järgmise seeria tegevusi:

1. Seadistage järgmised atribuudid tootmise konfiguratsiooni mudelis:

    - Sisestus (täisarv)
    - Protsent (kümnendarv)
    - Tulemus (täisarv)

2. Looge järgmiste sätetega kalkulatsioon:

    *Tulemus* = *sisend* × *protsent* ÷ 100

Sel juhul ei ümardata täisarvu tulemust alati õigesti. Näiteks on sisend 1 000 ja protsent on 2,40. Seetõttu eeldatakse, et tulemuse täisarv on 24, kuna 2,40 protsenti 1 000 on 24 (või 24,00 kümnendkoha vormis). Selle asemel kuvatakse tulemus 23. Kuid kui protsent on 2,39, ümardatakse arvutus 24 asemel 23-ni. Kui protsent on 2,50, ümardatakse arvutus 25-ni, nagu oodatud.

### <a name="issue-resolution"></a>Probleemi lahendamine

See probleem ilmneb seetõttu, et Microsoft Solver Foundation esindab sisemiselt numbreid, kasutades fraktsioone. Eelmise näite puhul on arvutuse tulemus, mille protsent on 2,40: 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375. Kui .NET annab selle väärtuse täisarvuna, tagastatakse see kui 23.

Seda käitumist ei muudeta, kuna teised stsenaariumid sõltuvad sellest. Eelneva näite puhul saate probleemi lahendada, kehtestades täiendava kümnendkoha atribuudi ja arvutuse.

Näiteks saate seadistada järgmised atribuudid tootmise konfiguratsiooni mudelis:

- Sisestus (täisarv)
- Protsent (kümnendarv)
- ResultDecimal (kümnendarv)
- ResultInteger (täisarv)

Seejärel saate lisada järgmisi arvutusi:

- *ResultDecimal* = *sisend* × *protsent* ÷ 100
- *ResultInteger* = *ResultDecimal*
