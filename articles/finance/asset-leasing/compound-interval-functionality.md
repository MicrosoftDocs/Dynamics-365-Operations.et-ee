---
title: Liitintervalli funktsioon
description: See artikkel annab teavet, mis aitab teil valida kuu, kvartali, poolaasta ja iga-aastase liitmisintervallide vahel.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2de5f1e9d52de41388298031a03fbc487a1b1cde
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886409"
---
# <a name="compounding-interval-functionality"></a>Liitintervalli funktsioon

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

See artikkel annab teavet, mis aitab teil valida kuu, kvartali, poolaasta ja iga-aastase liitmisintervallide vahel. Liitintervalli funktsiooni kasutatakse rendimaksete graafiku liitperioodide arvu määramiseks aastas. Iga nelja selle artikli näitest näitab, milline on rendi maksegraafik erineva intervalli puhul.

Te ei saa valida liitintervalli, mis on harvem kui rendimaksete sagedus. Näiteks ei saa kvartalipõhist liitintervalli kasutada koos igakuise maksesagedusega ja iga-aastast liitintervalli ei saa kasutada poolaastase maksesagedusega. Kui proovite valida liitintervalli, mis on harvem kui rendimaksete sagedus, kuvatakse tõrketeade.

> [!NOTE]
> Selle artikli kõigi nelja näite puhul ühtib liitmisintervall maksesagedusega.

## <a name="examples"></a>Näited

### <a name="setup-for-all-four-leases"></a>Kõigi nelja rendikirje häälestamine

Järgmistes tabelites on toodud väärtused, mis on määratud vahekaartidel **Üldine** ja **Maksegraafiku read** nelja rendikirje jaoks, mida näidetes kasutatakse.

**Vahekaart Üldine**

| Field                      | Väärtus                        |
|----------------------------|------------------------------|
| Alternatiivne laenuintressimäär | **5%**                       |
| Annuiteedi tüüp               | **Harilik annuiteet**         |
| Liitmisintervall       | Vaadake individuaalseid näiteid. |
| Makse sagedus          | **Kord kuus**                  |
| Alguskuupäev          | **1.1.2020**                 |

**Maksegraafiku ridade vahekaart**

| Field             | Väärtus                        |
|-------------------|------------------------------|
| Alguskuupäev        | **1.1.2020**                 |
| Perioodid           | **120**                      |
| Perioodi intervall   | **Kuud**                   |
| Lõppkuupäev          | **31.12.2029**               |
| Makse sagedus | Vaadake individuaalseid näiteid. |
| Maksesumma    | **50,000**                   |

### <a name="lease-1-monthly-compounding-interval-and-monthly-payment-frequency"></a>Rent 1: igakuine liitintervall ja igakuine maksesagedus

Järgmises tabelis on loetletud maksegraafiku esimesed 12 kuud. Arvestage järgmist.

- Veeru Periood väärtus suureneb ühe võrra iga kuu, kuna iga kuu on uus liitintervall.
- Valemi veeru Praegune väärtus määr on jagatud 12-ga, kuna aastas on 12 liitperioodi. Aste (st ülaindeks) võrdub veerus Periood oleva väärtusega.

| Periood | Kuu | Kuupäev       | Maksesumma | Praegune väärtus                                       |
|--------|-------|------------|----------------|-----------------------------------------------------|
| 1      | 1     | 31.1.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 12\])<sup>1</sup> = 49 792,53  |
| 2      | 2     | 29.2.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 12\])<sup>2</sup> = 49 585,92  |
| 3      | 3     | 31.3.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 12\])<sup>3</sup> = 49 380,17  |
| 4      | 4     | 30.4.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 12\])<sup>4</sup> = 49 175,28  |
| 5      | 5     | 31.5.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 12\])<sup>5</sup> = 48 971,23  |
| 6      | 6     | 30.6.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 12\])<sup>6</sup> = 48 768,03  |
| 7      | 7     | 31.7.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 12\])<sup>7</sup> = 48 565,67  |
| 8      | 8     | 31.8.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 12\])<sup>8</sup> = 48 364,15  |
| 9      | 9     | 30.9.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 12\])<sup>9</sup> = 48 163,47  |
| 10     | 10    | 31.10.2020 | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 12\])<sup>10</sup> = 47 963,62 |
| 11     | 11    | 30.11.2020 | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 12\])<sup>11</sup> = 47 764,61 |
| 12     | 12    | 31.12.2020 | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 12\])<sup>12</sup> = 47 566,41 |

### <a name="lease-2-quarterly-compounding-interval-and-quarterly-payment-frequency"></a>Rent 2: kvartalipõhine liitintervall ja kvartalipõhine maksesagedus

Järgmises tabelis on loetletud maksegraafiku esimesed 12 kuud. Arvestage järgmist.

- Veeru Periood väärtus suureneb ühe võrra iga kolme kuu tagant (st kord kvartalis), kuna iga kvartal on uus liitintervall.
- Valemi veeru Praegune väärtus määr on jagatud 4-ga, kuna aastas on neli liitperioodi. Aste võrdub veerus Periood oleva väärtusega.

| Periood | Kuu | Kuupäev       | Maksesumma | Praegune väärtus                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.1.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>1</sup> = 0           |
| 1      | 2     | 29.2.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>1</sup> = 0           |
| 1      | 3     | 31.3.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 4\])<sup>1</sup> = 49 382,72 |
| 2      | 4     | 30.4.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>2</sup> = 0           |
| 2      | 5     | 31.5.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>2</sup> = 0           |
| 2      | 6     | 30.6.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 4\])<sup>2</sup> = 48 773,05 |
| 3      | 7     | 31.7.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>3</sup> = 0           |
| 3      | 8     | 31.8.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>3</sup> = 0           |
| 3      | 9     | 30.9.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 4\])<sup>3</sup> = 48 170,92 |
| 4      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>4</sup> = 0           |
| 4      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 4\])<sup>4</sup> = 0           |
| 4      | 12    | 31.12.2020 | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 4\])<sup>4</sup> = 47 576,21 |

> [!NOTE]
> Kui annuiteedi tüübiks on määratud **Annuiteedi tähtaeg**, on makse kvartali lõpu asemel kvartali alguses.

### <a name="lease-3-semiannual-compounding-interval-and-semiannual-payment-frequency"></a>Rent 3: poolaastapõhine liitintervall ja poolaastapõhine maksesagedus

Järgmises tabelis on loetletud maksegraafiku esimesed 12 kuud. Arvestage järgmist.

- Veeru Periood väärtus suureneb ühe võrra iga kuue kuu tagant (st kaks korda aastas), kuna iga poolaasta on uus liitintervall.
- Valemi veeru Praegune väärtus määr on jagatud 2-ga, kuna aastas on kaks liitperioodi. Aste võrdub veerus Periood oleva väärtusega.

| Periood | Kuu | Kuupäev       | Maksesumma | Praegune väärtus                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.1.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 2     | 29.2.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 3     | 31.3.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 4     | 30.4.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 5     | 31.5.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 0           |
| 1      | 6     | 30.6.2020  | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 2\])<sup>1</sup> = 48 780,49 |
| 2      | 7     | 31.7.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 8     | 31.8.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 9     | 30.9.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 0           |
| 2      | 12    | 31.12.2020 | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 2\])<sup>2</sup> = 47 590,72 |

> [!NOTE]
> Kui annuiteedi tüüp muudetakse valikule **Annuiteedi tähtaeg**, tehakse maksed juuni ja detsembri asemel jaanuaris ja juulis.

### <a name="lease-4-annual-compounding-interval-and-annual-payment-frequency"></a>Rent 4: aastapõhine liitintervall ja aastapõhine maksesagedus

Järgmises tabelis on loetletud maksegraafiku esimesed 12 kuud. Arvestage järgmist.

- Veeru Periood väärtus suureneb ühe võrra iga 12 kuu tagant (st kord aastas), kuna iga aasta on uus liitintervall.
- Valemi veeru Praegune väärtus määr on jagatud 1-ga, kuna aastas on üks liitperiood. Aste võrdub veerus Periood oleva väärtusega.

| Periood | Kuu | Kuupäev       | Maksesumma | Praegune väärtus                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.1.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 2     | 29.2.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 3     | 31.3.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 4     | 30.4.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 5     | 31.5.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 6     | 30.6.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 7     | 31.7.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 8     | 31.8.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 9     | 30.9.2020  | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 0           |
| 1      | 12    | 31.12.2020 | 50,000.00      | 50 000 ÷ (1 + \[5% ÷ 1\])<sup>1</sup> = 47 619,05 |

> [!NOTE]
> Kui annuiteedi tüüp muudetakse valikule **Annuiteedi tähtaeg**, tehakse maksed detsembri asemel jaanuaris.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
