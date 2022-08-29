---
title: Arhiivi prinditud kliendiarved räsinumbritega
description: See artikkel selgitab, kuidas lubada prinditud kliendiarvete arhiveerimine koos hash numbers-dega.
author: mrolecki
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.custom: 539093
ms.search.form: ''
ms.openlocfilehash: 4c9bd7ead1615a4e6b0e8e672e858312ba518b56
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291665"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Arhiivi prinditud kliendiarved räsinumbritega

[!include [banner](../includes/banner.md)]

Mõnedes riikides on juriidiline nõue talletada süsteemis arvutatud räsinumbrid koos mõne dokumendi väljaprintiga. Räsinumbreid saab kasutada ametivõimudele aruandluseks ja auditi ajal.

See artikkel selgitab, kuidas konfigureerida arhiivimist, et talletada prinditud kliendiarved koos hash-numbritega.

## <a name="prerequisites"></a>Eeltingimused

- **Funktsioonihalduse** tööruumis lülitage funktsioon sisse, **arhiveerige prinditud kliendiarved koos numbriga**. Lisateavet vt [Funktsioonihalduse ülevaatest](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- **Prindihalduses** tuleb konfigureerida nõutud dokumentide prinditavad vormingud.

See funktsioon on rakendatav järgmiste dokumentide puhul.

**Müügireskontro**
- Kliendiarve
- Kliendi kreeditarve
- Vabas vormis arve
- Vabas vormis kreeditarve

**Projektihaldus ja -arvestus**
- Projektiarve
- Projekti kreeditarve

## <a name="configure-customer-master-data"></a>Kliendi koondandmete haldamine
Viige kliendi andmete konfigureerimiseks lõpule järgmised sammud ja lülitage sisse võimalus prinditud arved manustena automaatselt salvestada.

1. Avage **Saadaolevad arved** > **Kõik kliendid**. 
2. Valige klient ning valige **Arve ja kohaletoimetamine** kiirkaardil **E-arve**, jaotises **manus** valige **jah**.

## <a name="print-invoices"></a>Prindi arve
Saate eelmises protseduuris konfigureeritud kliendile sisestada ja printida vabas vormis, kliendi- ja projektiarve või kreeditarve.

Saate avada **Manused** prinditud arve lehe. **Manused** kiirkaardil **Täiendavad üksikasjad** väljal **Dokumendi räsinumber**, leidke prinditud arve jaoks salvestatud räsinumber.

![Manuse räsinumber.](media/attach-hash-num.jpg)

