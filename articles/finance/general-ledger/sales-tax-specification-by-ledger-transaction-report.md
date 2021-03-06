---
title: Käibemaksu täpsustus pearaamatu kannete aruande alusel
description: See teema selgitab, kuidas kasutada käibemaksu täpsustust pearaamatu kannete aruande alusel, et vaadata ja printida teavet pearaamatu kannete kohta, mille jaoks käibemaks arvutatakse.
author: ericwang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 75913edcbac0151d5d27d866ff5430b194c62738
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815256"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>Käibemaksu täpsustus pearaamatu kannete aruande alusel
[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas kasutada **käibemaksu täpsustust pearaamatu kannete** aruande alusel, et vaadata ja printida teavet pearaamatu kannete kohta, mille jaoks käibemaks arvutatakse.

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

![Mitte-maksukontosid näitav aruanne](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]