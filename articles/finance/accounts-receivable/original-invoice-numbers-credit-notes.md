---
title: Viited algsetele arvetele krediidiarvetes
description: Selles teemas kirjeldatakse, kuidas seadistada ja printida originaalarvete numbreid seotud kreeditarvetes.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 673288f04b33aa2a578f9e2e7913dbe7ac309644
ms.sourcegitcommit: 7cdec5469ff0da145ac4e01caf3287d0627ae2dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2021
ms.locfileid: "5099998"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Viited algsetele arvetele krediidiarvetes

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Mõnes riigis ja regioonis on juriidiline nõue, et prinditud kreeditarved sisaldavad viiteid originaalarvetele. Selles teemas kirjeldatakse, kuidas seadistada ja printida originaalarvete numbreid seotud kreeditarvetes.

## <a name="prerequisites"></a>Eeltingimused

- Lülitage tööruumis **Funktsioonihaldus** sisse funktsioon **Kreeditarvete paigutus müügi ja projekti arvete aruandlusele**. Lisateavet vt [Funktsioonihalduse ülevaatest](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).
- Prindihalduses tuleb konfigureerida nõutud dokumentide prinditavad vormingud.

Selles teemas kirjeldatud funktsionaalsus kehtib järgmiste dokumentide puhul.

**Müügireskontro**

- Vabas vormis kreeditarve
- Kliendi kreeditarve

**Projektihaldus ja -arvestus**

- Projekti kreeditarve

## <a name="configure-accounts-receivable-parameters"></a>Müügireskontro parameetrite konfigureerimine

Järgige neid samme, et seadistada parameeter, mis kontrollib, kas viited originaalarvetele prinditakse seotud kreeditarvetele.

1. Minge jaotisse **Müügireskontro** \> **Seadistus** \> **Müügireskontro parameetrid**.
2. Seadke vahekaardil **Värskendused** kiirkaardil **Arve** suvandi **Rakenda kreeditarve paigutus müügi ja projekti arvete aruannetele** väärtuseks **Jah**.

![Müügireskontro parameetrite konfigureerimine](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Viidete määratlemine originaalarvetele

Dokumenditüübil põhinevate algsete arvete viidete määratlemiseks kasutage järgmisi protseduure.

### <a name="free-text-credit-note"></a>Vabas vormis kreeditarve

1. Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.
2. Looge uus kreeditarve või valige olemasolev kreeditarve.
3. Avage arve.
4. Valige toimingupaani vahekaardil **Arve** grupis **Funktsioonid** suvand **Krediitarveldus**.
5. Sisestage viide algsele arvele ja valige paranduse põhjus.

![Vabas vormis arve viite määratlemine](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Kliendi kreeditarve

1. Avage **Müügireskontro** \> **Tellimused** \> **Kõik müügitellimused**.
2. Valige ja avage arveldatud müügitellimus, mida tuleb parandada.
3. Valige toimingupaani vahekaardil **Müük** grupis **Kreeditarve** suvand **Kreeditarve**.
4. Sisestage paranduse põhjus. Viide algsele arvele luuakse automaatselt.

![Müügitellimuse viite määratlemine](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Projekti kreeditarve

1. Avage **Projektihaldus ja raamatupidamine** \> **Projektiarved** \> **Projektiarved**.
2. Valige ja avage arveldatud projektiarve, mida tuleb parandada.
3. Valige toimingupaani vahekaardil **Projektiarve** grupis **Funktsioonid** suvand **Vali kreeditarve jaoks**.
4. Valige **Kreeditarveldus**.
5. Sisestage paranduse põhjus. Viide algsele arvele luuakse automaatselt.

![Projekti arve viite määratlemine](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Kreeditarvete printimine

Kui prindite vaba teksti, kliendi ja projekti kreeditarved, sisaldavad need viidet originaalarvele ja paranduse põhjust.

![Prinditud kreeditarve](media/credit-note-FTI.jpg)

> [!NOTE]
> Veenduge, et dokumentide prinditavad vormingud on õigesti konfigureeritud, eeldusel, et prinditakse viited originaalarvetele.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]