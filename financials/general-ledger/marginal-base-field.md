---
title: "Käibemaksumäärad väljade Marginaali alus ja Arvutusmeetod põhjal"
description: "Selles artiklis selgitatakse, kuidas väljade Marginaali alus ja Arvutamismeetod väärtused määravad müügi- ja ostukannete maksumäära(d)."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: e16e91208cdd6c1a5c904fb763454371b02c71fd
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>Käibemaksumäärad väljade Marginaali alus ja Arvutusmeetod põhjal

[!include[banner](../includes/banner.md)]


Selles artiklis selgitatakse, kuidas väljade Marginaali alus ja Arvutamismeetod väärtused määravad müügi- ja ostukannete maksumäära(d).

Lehe Käibemaksukoodid kiirkaardil Arvutus olev väli Marginaali alus määrab, millist summat kasutatakse sobiva(te) maksumäära(de) valimiseks lehel Käibemaksukoodi väärtused olevate määrade hulgast. Väljal Marginaali alus olev summa tüüp koos meetodiga väljal Arvutusmeetod määrab kandele õige(te) maksumäära(de) leidmise loogika. 

Erinevad väärtuste kombinatsioonid nendel väljadel annavad tulemuseks väga erinevad käibemaksu kalkulatsioonid, nagu näha järgmistes näidetes. Näidetes kasutatakse samu maksu intervallväärtusi, mis on seadistatud iga maksukoodi jaoks lehel Käibemaksukoodide väärtused. Selle lehe avamiseks klõpsake lehel Käibemaksukoodid valikuid Käibemaksukood &gt; Väärtused.

> [!Important]                                                                                                                  
> Kui Marginaali alus või mõni käibemaksukood põhineb reasummadel või ühikutel, tuleb lehel Pearaamatu parameetrid määrata välja Arvutusmeetod väärtuseks Rida. |

## <a name="net-amount-per-line"></a> Netosumma rea kohta
Tehke see valik käibemaksumäärade arvutamiseks arve ridade netosumma alusel, välistades kõik muud maksud.

### <a name="example"></a>Näide

Käibemaksumäärad seadistatakse järgmiste intervallidega.

| summa intervall    | Maksumäär |
|--------------------|----------|
| 0–50             | 30%      |
| 50 – 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

> [!NOTE]                                                                                                             
> Viimase intervalli ülempiir null (0) tähendab, et kõik 100-st suuremad summad kaasatakse sellesse intervalli.

Marginaali alus: **Netosumma rea kohta** 

Arvutamismeetod: **Intervall** 

Ostate 8 lampi, mis maksavad 25.00 eurot tükk. 

Arve rea netosumma on 200.00 eurot. 

Käibemaks arvutatakse järgmiselt: 

Käibemaksu kogusumma = 50 × 30% + 50 × 20% + 100 × 10% = 15 + 10 + 10 = 35.00. 

Arve kogusumma = 200.00 + 35.00 = 235.00. 

**Kõikumine** 

Kui arvel on kaks rida, millest igal real on neli kaupa, on iga rea netosumma 100.00 ja käibemaks arvutatakse järgmiselt. 

Käibemaksu rida 1 = 50 × 30% + 50 × 20% = 15 + 10 = 25.00 

Käibemaksu rida 2 = 50 × 30% + 50 × 20% = 15 + 10 = 25.00. 

Käibemaks kokku = 25.00 + 25.00 = 50.00 

Arve kogusumma = 200.00 + 50.00 = 250.00

## <a name="net-amount-per-unit"></a> Netosumma ühiku kohta
Tehke see valik käibemaksumäärade määramiseks iga ühiku väärtuse alusel, jättes muud maksud välja. Kui on valitud ühikupõhine marginaali alus, tuleb käibemaksukoodile määrata ka ühik.

### <a name="example"></a>Näide

Käibemaksumäärad seadistatakse järgmiste intervallidega.

| Summa             | Maksumäär |
|--------------------|----------|
| 0–50             | 30%      |
| 50 – 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Marginaali alus: **Netosumma ühiku kohta** 

Arvutamismeetod = **terve summa** 

Ostate 8 lampi, mis maksavad 25.00 eurot tükk. 

Arve rea netosumma on 200.00 eurot. 

Käibemaks arvutatakse järgmiselt: käibemaks ühiku kohta = 25.00 x 30% = 7.50 Käibemaks kokku = 7.50 x 8 ühikut = 60.00 Arve koondsumma = 200.00 + 60.00 = 260.00

## <a name="net-amount-of-invoice-balance"></a> Arve saldo netosumma

Tehke see valik käibemaksumäärade arvutamiseks arve koondväärtuse alusel, välistades kõik muud maksud.

### <a name="example"></a>Näide

Käibemaksumäärad seadistatakse järgmiste intervallidega.

| Summa            | Maksumäär |
|-------------------|----------|
| 0–50            | 30%      |
| 50 – 100          | 20%      |
| 100 -0 (&gt; 100) | 10%      |

Marginaali alus: **arve saldo netosumma** 

Arvutamismeetod: **intervall** Müügiarvel on 2 rida, millest igal real on 4 lampi hinnaga 25.00. Arve saldo netosumma on 4 x 25.00 + 4 x 25.00 = 200.00. Käibemaks arvutatakse järgmiselt: käibemaksu koondsumma = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Arve koondsumma = 200.00 + 35.00 = 235.00

## <a name="gross-amount-per-line"></a> Brutosumma rea kohta

Tehke see valik käibemaksumäärade arvutamiseks arve rea väärtuse alusel, kaasates kõik muud selle rea maksud.

> [!NOTE]
> Käibemaksugrupis saab teil selle valiku puhul olla ainult üks käibemaksukood väljal Marginaali alus.

### <a name="example"></a>Näide

Käibemaksumäärad seadistatakse järgmiste intervallidega.

| Summa             | Maksumäär |
|--------------------|----------|
| 0–50             | 30%      |
| 50 – 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Marginaali alus: **brutosumma rea kohta** Arvutusmeetod: **intervall** Lisaks on veel üks maksukood, millega arvutatakse erilõiv 5.00 iga lambi kohta. Lõiv lisatakse netosummale enne käibemaksu arvutamist. Ostate 8 lampi, mis maksavad 25.00 eurot tükk. Arve rea netosumma on 200.00 eurot. Arverea brutosumma on 8 x 25.00 + 8 x 5.00 = 240.00 eurot. Käibemaks arvutatakse järgmiselt: käibemaksu koondsumma = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Lõiv kokku = 5.00 x 8 = 40.00 Arve summa kokku = 200.00 + 39.00 + 40.00 = 279.00

**Kõikumine** 

Kui arve koostatakse 2 arvereaga, millest igal real on 4 kaupa, on netosumma arve rea kohta 100.00. Brutosumma (sh lõiv 4 x 5.00) arve rea kohta oleks 120.00 ja käibemaks luuakse järgmiselt 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Käibemaksuarve rida 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Käibemaks kokku = 27.00 + 27.00 = 54.00 Lõiv kokku = 5.00 x 8 = 40.00 Arve summa kokku = 200.00 + 54.00 + 40.00 = 294.00

## <a name="gross-amount-per-unit"></a> Brutosumma ühiku kohta

Tehke see valik käibemaksumäärade määramiseks iga ühiku väärtuse alusel, kaasates kõik muud maksud.

> [!NOTE]
> Käibemaksugrupis saab teil selle valiku puhul olla ainult üks käibemaksukood väljal Marginaali alus.

### <a name="example"></a>Näide

Käibemaksumäärad seadistatakse järgmiste intervallidega.

| Summa             | Maksumäär |
|--------------------|----------|
| 0–50             | 30%      |
| 50 – 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Marginaali alus: **ühiku brutosumma** Iga lambi kohta kehtib erilõiv 5.00. Lõiv lisatakse netosummale enne käibemaksu arvutamist. Ostate 8 lampi, mis maksavad 25.00 eurot tükk. Ühiku brutosumma on 30.00. Maks arvutatakse järgmiselt: käibemaks ühiku kohta = 30 x 30% = 9.00 Käibemaks kokku = 9.00 x 8 = 72.00 Lõiv kokku = 5.00 x 8 = 40.00 Arve koondsumma = 200.00 + 72.00 + 40.00 = 312.00

## <a name="invoice-total-incl-other-sales-tax-amounts"></a> Arve kokku, sh muud käibemaksusummad

Tehke see valik käibemaksumäärade arvutamiseks arve koondväärtuse alusel, kaasates kõik muud maksud.
> [!NOTE]
> Käibemaksugrupis saab teil selle valiku puhul olla ainult üks käibemaksukood väljal Marginaali alus

### <a name="example"></a>Näide

Käibemaksumäärad seadistatakse järgmiste intervallidega.

| Summa             | Maksumäär |
|--------------------|----------|
| 0–50             | 30%      |
| 50 – 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Marginaali alus: **arve koondsumma, sh muud käibemaksusummad** Arvutusmeetod: **intervall**   
Iga lambi kohta kehtib erilõiv 5.00. Lõiv lisatakse netosummale enne käibemaksu arvutamist. Ostate 8 lampi, mis maksavad 25.00 eurot tükk. Arve netosumma on 200.00 eurot. Arve brutosumma on 200.00 + (8 x 5.00) = 240.00. Käibemaks arvutatakse järgmiselt: käibemaksu koondsumma = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Lõiv kokku = 5.00 x 8 = 40.00 Arve summa kokku = 200.00 + 39.00 + 40.00 = 279.00

Lisateavet leiate jaotisest [Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul](whole-amount-interval-options-sales-tax-codes.md) [Käibemaksu arvutusmeetodid väljal Päritolu](sales-tax-calculation-methods-origin-field.md).




