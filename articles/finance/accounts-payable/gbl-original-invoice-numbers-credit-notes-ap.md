---
title: Viidake algsetele arvetele kreeditarvetes (hankija arved)
description: See artikkel kirjeldab, kuidas luua kreeditarve loomisel viidet originaalarvele.
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e05dddf056d86513d86ea925349f60ca25f191ca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901485"
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
