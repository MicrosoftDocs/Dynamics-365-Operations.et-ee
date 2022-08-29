---
title: Viidake algsetele arvetele kreeditarvetes (hankija arved)
description: See artikkel kirjeldab, kuidas luua kreeditarve loomisel viidet originaalarvele.
author: AdamTrukawka
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.search.form: ''
ms.openlocfilehash: ed07ae9784da3ca721fcb25a9c5a14c4f75f2e59
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277366"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Viidake algsetele arvetele kreeditarvetes (hankija arved)

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas luua kreeditarve loomisel viidet originaalarvele.

## <a name="prerequisites"></a>Eeltingimused

Tööruumis **Funktsioonihaldus** valige **Luba müüja arvetel krediidiarvete esitamine** funktsioon. Lisateavet vt [Funktsioonihalduse ülevaatest](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Selles artiklis kirjeldatud funktsioonid kehtivad järgmiste äridokumentide puhul.

**Ostureskontro:**

- Ostutellimus
- Arve tööleht
- Arveregister

**Pearaamat:**

- Päevaraamat

## <a name="define-a-reference-to-an-original-invoice"></a>Määratlege viide originaalarvele

Kasutage järgmisi protseduure, et määratleda viide originaalarvele määratud äridokumendi tüüpides.

### <a name="vendor-credit-note-purchase-order"></a>Hankija kreeditarve (ostutellimus)

1. Avage jaotis **Ostureskontro** \> **Ostutellimused** \> **Kõik ostutellimused**.
2. Looge uus ostutellimus või kasutage olemasolevat kreeditarve loomiseks.
3. Valige toimingupaani vahekaardil **Arve** grupis **Tutvustamine** suvand **Krediitarveldus**.
4. Sisestage paranduse põhjus ja viide originaalarvele.

### <a name="vendor-credit-note-ledger-journals"></a>Hankija kreeditarve (pearaamatu töölehed)

1. Järgige üht neist sammudest.

    - Minge **Ostureskontro** \> **Arvete töölehed**.
    - Minge **Ostureskontro** \> **Arvete register**.
    - Minge **Pearaamat** \> **Töölehe kanded** \> **Päevaraamatud**.

2. Uue töölehe ja tööleheridade loomine.
3. Tegevuspaanil valige **Funktsioonid** \> **Krediidiarvete esitamine**.
4. Sisestage paranduse põhjus ja viide originaalarvele.

> [!NOTE]
> Käsk **Krediidiarvete esitamine** on nähtav ajakirjade üldvautšeris, kui väli **Kontotüüp** on seatud väärtusele **Müüja**.
