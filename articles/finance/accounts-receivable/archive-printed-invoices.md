---
title: Arhiivi prinditud kliendi arved räsinumbritega
description: See teema kirjeldab, kuidas lubada arhiveerimine, et talletada prinditud kliendiarved koos räsinumbritega.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c627b6238a5c0ec1a45ebd9692aae7c634c4952e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356795"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Arhiivi prinditud kliendi arved räsinumbritega

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Mõnedes riikides on juriidiline nõue talletada süsteemis arvutatud räsinumbrid koos mõne dokumendi väljaprintiga. Räsinumbreid saab kasutada ametivõimudele aruandluseks ja auditi ajal.

See teema kirjeldab, kuidas lubada arhiveerimine, et talletada prinditud kliendiarved koos räsinumbritega.

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

