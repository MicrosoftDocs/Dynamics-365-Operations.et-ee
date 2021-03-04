---
title: Kasutamisõiguse esemeks oleva vara kulumi kirjendamine (eelversioon)
description: Selles teemas selgitatakse, kuidas luua töölehe kirjet amortisatsioonile, mida on vaja organisatsiooni bilansis tuvastatud rentimistele.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0dd8308acb875affc96ca6d9ed856d74d4b2eb37
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442558"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a>Kasutamisõiguse esemeks oleva vara kulumi kirjendamine (eelversioon)

[!include [banner](../includes/banner.md)]

Organisatsiooni bilansis tuvastatud rentide korral, amortiseeritakse kasutamisõiguse esemeks olevat vara igakuiselt. Selles teemas selgitatakse, kuidas luua amortisatsioonile töölehe kirjet. Amortisatsioon debiteerib pearaamatu kulukonto ja krediteerib pearaamatu akumuleeritud kulumi konto vastavalt sisestusprofiili seadistusele ja rendi tüübile. Neid kirjeid saab luua iga rendilepingu jaoks või luua mitmele rendilepingule, kasutades pakett-töölehe funktsiooni.

## <a name="asset-depreciation-schedule"></a>Vara kulumigraafik

1. Valige **Rendi kokkuvõtte** lehel rendileping. Seejärel valige **Raamatud \> Vara kulumigraafik**, et avada leht **Vara kulumigraafik**.

    Kasutamisõiguse esemeks oleva vara kulumi töölehe kirje põhineb veerus **Kulumi kulu** oleval summal. Raamatupidamise standardi vastavuse juhendite näite leiate edaspidi selles teemas olevast jaotisest [Kasutamisõiguse esemeks oleva vara amortisatsiooni kulumi arvutamine kapitalirendi korral](#calculation-of-rou-asset-amortization-expense-for-finance-leases).

2. Valige kulumi periood ja seejärel valige **Loo tööleht**. Kuvatakse teade, mis teatab, et tööleht, mida kasutatakse kulumi kirjendamiseks, on loodud.
3. Valige **Töölehed \> Vara rentimise töölehed**, et avada leht **Vara rentimise tööleht**, kus saate vaadata loodud kulumi töölehe kirjet.
4. Valige töölehe kirje ja seejärel valige kulumi kirje pearaamatusse kandmiseks käsk **Sisesta**.

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a>Kasutamisõiguse esemeks oleva vara amortisatiooni kulu arvutamine kasutusrendi korral

Kasutusrendi kulumi kulu arvutatakse igakuise lineaarse rendikulu ja intressikulu vahena vastavalt raamatupidamise standarditele kodifitseerimise teemale 842 (ASC 842), mis on üldtunnustatud raamatupidamispõhimõtete kohaselt standardiks USA-s (US GAAP). Lineaarse rendikulu arvutamiseks jagatakse kõigi rendimaksete summa rendiperioodiga kuudes. (Rendimaksete summa sisaldab mis tahes ettemakseid, esmaseid otsekulutusi, demonteerimiskulusid ja rendistiimuleid.) Järgmine tabel näitab kasutusrendi amortisatsiooni kulu näidet.

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a>Kasutamisõiguse esemeks oleva vara amortisatiooni kulu näide kasutusrendi korral

| Field                                          | Väärtus       |
|------------------------------------------------|-------------|
| Maksesumma                                 | 1000       |
| Makse sagedus                              | Kord kuus     |
| Rendiperiood (kuudes)                            | 24          |
| Rendimaksete kogusumma                           | 24,000      |
| Alternatiivne laenuintressimäär                     | 5%          |
| Annuiteedi tüüp                                   | Avansiline annuiteet |
| Liitmisintervall                           | Kord kuus     |
| Tulevaste minimaalsete rendimaksete praegune väärtus | 22,888.87   |

Nagu varem mainitud, siis lineaarse rendikulu arvutamiseks jagatakse kõigi maksete summa rendiperioodiga. Süsteem arvutab igakuise intressikulu automaatselt rendikohustise amortisatsioonigraafiku järgi. Intressikulu arvutatakse kasutades kehtivat intressimäära meetodit. Süsteem kasutab iga kuu intressikulu lahutamiseks lineaarset rendikulu. Väärtust kasutatakse kasutamisõiguse esemeks oleva vara vähendamiseks.

| Kuu | Lineaarne rendikulu | Intressikulu                        | Kasutamisõiguse esemeks oleva vara amortisatsiooni kulu arvutamine |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| 1     | (24000 ÷ 24) = 1000,00 | (22888,87 – 1000) × (5% ÷ 12) = 91,20 | 1000 – 91,20 = 908,80                        |
| 2     | (24000 ÷ 24) = 1000,00 | (21980.08 – 1000) × (5% ÷ 12) = 87,42 | 1000 – 87,42 = 912,58                        |
| 3     | (24000 ÷ 24) = 1000,00 | (21067,49 – 1000) × (5% ÷ 12) = 83,62 | 1000 – 83,62 = 916,39                        |

> [!NOTE]
> Vastavalt ASC 842-le on kasutusrendi kasutamisõiguse esemeks oleva vara kulum kasumiaruandes liigitatud rendikuluna. Nähtavuse saamiseks kirjeldab vara rentimine kirjet kasutamisõiguse esemeks oleva vara kulumina. Kuid deebetkanne tuleks määrata kasutusrendi kulukontole ja kreeditkanne tuleks määrata otse kasutamisõiguse esemeks oleva vara kasutusrendile. Sellegipoolest saate rendi parameetrites määrata, et kasutamisõiguse esemeks oleva vara puhul tuleks akumuleeritud kulumi kontole kreeditkandeid teha.

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a>Kasutamisõiguse esemeks oleva vara amortisatiooni kulu arvutamine kapitalirendi korral

Kapitalirendi klassifikatsiooni korral arvutab süsteem kasutamisõiguse esemeks oleva vara amortisatsiooni lineaarsel alusel. Seetõttu on kulumi kulu igas kuus sama.

Vastavalt rahvusvahelise finantsaruandluse standarditele 16 (IFRS 16) ja ASC 842 on vara amortiseeritud kas rendiperioodi jooksul või vara kasuliku eluea jooksul, olenevalt sellest, kumb on lühem. Lisaks, kui rendilepingu parameeter **Omandiõiguse üleminek** on sisse lülitatud, amortiseerub rendileping automaatselt vara kasuliku eluea jooksul.

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a>Kasutamisõiguse esemeks oleva vara amortisatiooni kulu näide kapitalirendi korral

| Field                                | Väärtus                                   |
|--------------------------------------|-----------------------------------------|
| Kasutamisõiguse esemeks oleva vara saldo algus | 22,889.87                               |
| Rendiperiood (kuudes)                  | 24                                      |
| Vara kasulik tööiga (kuudes)           | 36                                      |
| Kuu                                | Kasutamisõiguse esemeks oleva vara amortisatsiooni kulu |
| 1                                    | 22889,87 ÷ 24 = 953,74                 |
| 2                                    | 22889,87 ÷ 24 = 953,74                 |
| 3                                    | 22889,87 ÷ 24 = 953,74                 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]