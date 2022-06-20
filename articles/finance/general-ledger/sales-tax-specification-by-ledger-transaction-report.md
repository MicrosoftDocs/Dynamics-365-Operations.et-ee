---
title: Käibemaksu täpsustus pearaamatu kannete aruande alusel
description: See artikkel selgitab, kuidas kasutada pearaamatukande aruande käibemaksu täpsustust, et vaadata ja printida teavet pearaamatu kannete kohta, mille jaoks käibemaksu arvutatakse.
author: EricWang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: c96f457a0ea24aef1769f370c3c0657ada31eebf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898087"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>Käibemaksu täpsustus pearaamatu kannete aruande alusel
[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas kasutada **pearaamatukande** aruande käibemaksu täpsustust, et vaadata ja printida teavet pearaamatu kannete kohta, mille jaoks käibemaksu arvutatakse.

## <a name="tax-accounts-vs-non-tax-accounts"></a>Maksukontod vs mitte-maksukontod

**Käibemaksu täpsustus pearaamatu kannete** aruande alusel näitab nii maksukontode kui ka mitte-maksukontode kandeid. Need kontod on kategoriseeritud järgmisel viisil.

- **Maksukonto** – kontot peetakse maksukontoks, kui maksukanne on sisestatud ja **Käibemaksu** töölehe real olev põhikonto on maksukonto, nt tasumisele kuuluva käibemaksu konto või saadaoleva käibemaksu konto.
- **Mitte-maksukonto** – kontot peetakse mitte-maksukontoks, kui maksukanne on sisestatud ja algse kande põhikonto on mitte-maksukonto, näiteks ja Käibemaksu töölehe real olev põhikonto on maksukonto, nt tulukonto või kulukonto.

Maksukontode korral näitavad veerud **Päritolu**, **Saadaolev käibemaks** ja **Tasumisele kuuluv käibemaks** aruandel väärtust **0** (null). Mitte-maksukontodekorral näitavad need veerud summasid.

## <a name="filtering-the-data-on-the-report"></a>Aruande andmete filtreerimine

Aruande loomisel on saadaval järgmised vaikeväljad. Saate neid välju kasutada aruandel kuvatavate andmete filtreerimiseks.

| Väli                      | Kirjeldus |
|----------------------------|-------------|
| Kuupäev                       | Kasutage jaotiste **Alates** ja **Kuni** välju, et määratleda maksukannete kuupäevavahemik. |
| Põhikonto               | Kasutage jaotiste **Alates** ja **Kuni** välju, et määratleda põhikontode vahemik. |
| Käibemaksukood             | Kasutage jaotiste **Alates** ja **Kuni** välju, et määratleda käibemaksukoodide vahemik. |
| Grupeerimine                   | Valige, kas aruanne peaks olema grupeeritud pearaamatu konto või käibemaksukoodi järgi. |
| Vahesumma käibemaksukoodide kaupa | Seadistage see suvand olekusse **Jah**, et kuvada vahesummad käibemaksukoodide kaupa. |
| Ainult kogusummad                | Seadistage see suvand olekusse **Jah**, et kuvada ainult kogusummasid. |
| Ainult põhikontod         | Seadistage see suvand olekusse **Jah**, et kaasata aruandesse ainult põhikontod. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>Aruandes ainult mitte-maksukontode kuvamine

Aruandes ainult mitte-maksukontode kuvamiseks seadistage filtri tingimus, nt asterisk (\*), nii nagu näidatud järgmisel joonisel.

![Mitte-maksukontosid näitav aruanne.](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
