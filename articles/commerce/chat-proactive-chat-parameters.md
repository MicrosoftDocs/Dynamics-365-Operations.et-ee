---
title: Ärivestluse mooduli ennetavad vestluseparameetrid
description: See artikkel kirjeldab Ärivestlusmoodulite ennetavat vestlusparameetrit moodulis Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690947"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>Ärivestluse mooduli ennetavad vestluseparameetrid

[!include [banner](includes/banner.md)]

See artikkel kirjeldab klienditeeninduse ja ärivestluse (koos vestlusmoodulitega Commerce Vestlus) klienditeeninduse ja ärivestluse moodulitega ärivestluse parameetreid teemas .Power Virtual Agents Microsoft Dynamics 365 Commerce

## <a name="proactive-chat-properties"></a>Ennetava vestluse atribuudid

Ennetav vestlusassead asuvad Commerce Commerce Commerce’i ja Klienditeeninduse rakenduse Commerce Commerce Commerce koosmoodulite atribuutide paanil Commerce CommerceChannel for Customer Service ja Commerce Commerce Commerce Koos Power Virtual Agents moodulitega Commerce site builderis.

> [!NOTE]
> Vaikimisi on kõik siin loetletud ennetava vestluse atribuudid tühjad. Soovitame teil nende atribuutide kohta rohkem teada saada ja neid vastavalt vajadusele seadistada. See lähenemine aitab vähendada vigaseid proaktiivseid vestlusi käivitamist.

### <a name="proactive-chat"></a>Ennetav vestlus

| Hüüdnimi | Kirjeldus | Vaikeväärtus |
|---------------|-------------|---------------|
| Lubatud | Saate erinevate päästikute alusel ennetavalt kaasata kliente. | Keelatud |
| Vestlusetervitus | Hoiatusteade, mida kasutatakse ennetava vestluse käivitamisel. | Tühi |

### <a name="wait-time-proactive-chat"></a>Ooteaeg (ennetav vestlus)

| Hüüdnimi | Kirjeldus |
|---------------|-------------|
| Ooteaeg (sek) | Aeg (sekundites), mille saidi kasutajad kulutada saidi lehel enne enne proaktiivse vestluse käivitamist. |
| Vestlusetervitus | Hoiatusteade, mida kasutatakse ennetava vestluse käivitamisel. |

### <a name="number-of-page-visits-proactive-chat"></a>Leheküljekülastuste arv (ennetav vestlus)

| Hüüdnimi | Kirjeldus |
|---------------|-------------|
| Leheküljekülastuste arv | Leheküljekülastuste arv enne enne enne proaktiivse vestluse käivitamist. Saidi kasutajad peavad kõigepealt nõustuma küpsistega nõustumise käsuga. |
| Vestlusetervitus | Hoiatusteade, mida kasutatakse ennetava vestluse käivitamisel. |

### <a name="specific-pages-proactive-chat"></a>Kindlad leheküljed (ennetav vestlus)

| Hüüdnimi | Kirjeldus |
|---------------|-------------|
| Leheküljed | Loend lehtedest, mis käivitavad külastamisel ennetava vestluse. |
| Vestlusetervitus | Hoiatusteade, mida kasutatakse ennetava vestluse käivitamisel. |

### <a name="from-specific-pages-proactive-chat"></a>Kindlatelt lehtedelt (ennetav vestlus)

| Hüüdnimi | Kirjeldus |
|---------------|-------------|
| Leheküljed | Loend lehtedest, mis käivitavad ennetava vestluse, kui kasutajad neist eemal navigeerivad. |
| Vestlusetervitus | Hoiatusteade, mida kasutatakse ennetava vestluse käivitamisel. |

### <a name="specific-countryregion-proactive-chat"></a>Konkreetne riik/regioon (ennetav vestlus)

| Hüüdnimi | Kirjeldus |
|---------------|-------------|
| Riigi kood | Kasutajad, kes külastavad määratud riike või piirkondi, käivitavad ennetava vestluse. Riigi-/regioonikoodid peaksid olema kaks suurtähte (nt **USA**). |
| Vestlusetervitus | Hoiatusteade, mida kasutatakse ennetava vestluse käivitamisel. |

### <a name="date-range-proactive-chat"></a>Kuupäevavahemik (ennetav vestlus)

| Hüüdnimi | Kirjeldus |
|---------------|-------------|
| Alguskuupäev (pp/kk/aaaa) | Kuupäev, millal või pärast seda ennetav vestlus käivitatakse. |
| Lõppkuupäev (pp/kk/aaaa) | Kuupäev, mis ajal või enne enne proaktiivse vestluse käivitamist käivitatakse. |
| Vestlusetervitus | Hoiatusteade, mida kasutatakse ennetava vestluse käivitamisel. |

### <a name="total-amount-in-cart-proactive-chat"></a>Ostukorvis kogusumma (ennetav vestlus)

| Hüüdnimi | Kirjeldus |
|---------------|-------------|
| Miinimum | Minimaalne rahasumma (k.a), mis käivitab ennetava vestluse, kui kasutajad ostukorvi lehte külastavad. |
| Maksimum | Maksimaalne rahasumma (s.h), mis käivitab ennetava vestluse, kui kasutajad ostukorvi lehte külastavad. |
|Vestlusetervitus | Hoiatusteade, mida kasutatakse ennetava vestluse käivitamisel. |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>Ostukorvis olevate kaupade koguarv (ennetav vestlus)

| Hüüdnimi | Kirjeldus |
|---------------|-------------|
| Miinimum | Minimaalne kaupade arv (s.h), mis käivitab ennetava vestluse, kui kasutajad ostukorvi lehte külastavad. |
| Maksimum | Maksimaalne kaupade arv (s.h), mis käivitab ennetava vestluse, kui kasutajad ostukorvi lehte külastavad. |
| Vestlusetervitus | Hoiatusteade, mida kasutatakse ennetava vestluse käivitamisel. |

### <a name="specific-products-in-cart-proactive-chat"></a>Kindlad tooted ostukorvis (ennetav vestlus)

| Hüüdnimi | Kirjeldus |
|---------------|-------------|
| Toodete ID/SKU | Toote ID-de/varude raamatupidamisühikute (SKU) numbrite loend, mis käivitab ennetava vestluse, kui kasutajad külastavad ostukorvi lehekülge. |
| Vestlusetervitus | Hoiatusteade, mida kasutatakse ennetava vestluse käivitamisel. |

## <a name="additional-resources"></a>Lisaressursid

[Ärivestluse funktsioonide ülevaade](commerce-chat-overview.md)

[Ärivestlus Koos Dllchanneliga klienditeeninduse mooduli jaoks](commerce-chat-module.md)

[Ärivestlus mooduliga Power Virtual Agents](chat-module-pva.md)
