---
title: Koondplaneerimise kaupu ei saa filtreerida seotud laovarude grupi väärtuste alusel
description: Koondplaneerimise kaupu ei saa filtreerida seotud laovarude grupi väärtuste alusel.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049463"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>Koondplaneerimise kaupu ei saa filtreerida seotud laovarude grupi väärtuste alusel

KB number: 4612572

## <a name="symptoms"></a>Sümptomid

Te soovite filtreerida kaupu, mis kaasatakse koondplaneerimise pakett-töösse, mis põhineb kauba laovarude tabeli seotud kirjete väärtustel. (Näiteks soovite üksusi filtreerida nende järgi **Hankija** ja/või **laovarude grupi** väärtus). Pakktöö filtri seadistus võimaldab luua ühenduse tabelist **Kaubad** laovarude tabeliga **Laovarude tabeliga** ja seejärel määrata päringu kauba laovarude tabeli väljaväärtused. Kuid pärast selle seadistuse lõpule viimist loob süsteem siiski plaanitud tellimused kogu kauba laovarudele, mitte ainult kaupadele, mis vastavad kauba laovarude tabeli määratud välja väärtustele.

## <a name="resolution"></a>Lahendus

Pakett-töö filter saab filtreerida ainult kaupade puhul. Kuigi saate lisada liitmise **kauba laovarude tabelile** ei mõjuta selle tabeli suhtes soovitudfiltrisätted päringu väljundit. Käitusajal käitab süsteem kõigi laovarude gruppide ja kõigi filtreeritud kaupade variatsioonide planeerimist. Kui kaup on juba käituse kaasatud, ei mõjuta ükski kaubafiltrisse kaasatud laovarude grupp plaanimise väljundit.
