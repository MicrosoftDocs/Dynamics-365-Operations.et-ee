---
title: Mõõteühiku teisendus tootevariandi kohta
description: See teema kirjeldab, kuidas saab seadistada tootevariantide mõõtühikute teisendusi.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 196b68db02867f8d864be8bcc593aa01f554f7c3
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249444"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Mõõteühiku teisendus tootevariandi kohta

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

See teema kirjeldab, kuidas saab seadistada tootevariantide mõõtühikute teisendusi. See sisaldab seadistuse näidet.

Funktsioon võimaldab ettevõtetel määratleda erinevaid ühikuteisendusi sama kauba variantide vahel. Selles teemas kasutatakse järgmist näidet. Ettevõte müüb t-särke suuruses S, M, L ja XL. T-särgi määratletakse tootena ja erinevad suurused määratletakse toote variantidena. T-särgid on pakendatud kastidesse ja ühes kastis võib olla viis t-särki, välja arvatud XL suurus, kus on ruumi ainult neljale t-särgile. Ettevõte soovib jälgida t-särkide erinevaid variante üksuses **Tükid**, aga müüb T-särke üksuses **Kastid**. Teisendused laoüksuse ja müügiüksuse vahel on 1 kast = 5 tükki, välja arvatud variant XL, kus teisendus on 1 kast = 4 tükki.

## <a name="setup"></a>Seadistus

Saate konfigureerida parameetrid funktsiooni kasutamiseks kas toodetele, mille puhul on lubatud **Kõik protsessid** või ainult tootele, mille puhul on lubatud **Lao protsessid**, kasutades suvandit **Luba mõõtühiku teisaldamine** lehel **Tooteteabe parameetrid**.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Seadistage toode ühiku teisaldamiseks varjandi kohta

Tootevariantide saab luua ainult toodetele **Toote alamtüüp**: **Tooteetalon**. Lisateavet vt jaotisest [Tooteetaloni loomine](tasks/create-product-master.md).

Funktsioon ei ole lubatud toodete puhul, mis on seadistatud tegeliku kaalu protsesside jaoks. 

Tooteetaloni loomise ajal lubage mõõtühiku teisendamine, kasutades suvandit **Luba mõõtühiku teisendused** lehel **Toote üksikasjad**.

Kui tooteetalon koos väljastatud toodete variantidega on loodud, saab seadistada ühikuteisendused variantide kohta. Toote või tootevariandi kontekstis toimuvate ühikuteisenduste avamise menüüelemendi leiate järgmistel lehekülgedelt.

-   Leht **Toote üksikasjad**
-   Leht **Väljastatud toodete üksikasjad**
-   Leht **Väljastatud toodete variandid**

Kui avate lehe **Ühikuteisendused** tooteetaloni kontekstis või väljastatud tootevariandi konstekstis, võite valida, kas soovite seadistada ühikuteisenduse tootele või tootevariandile. Seda saate teha valides kas **Tootevariant** või **Toode** väljal **Loo teisendus:**.

### <a name="product-variant"></a>Tootevariant

Kui valite valiku **Tootevariant**, siis saate valida, millisele variandile soovite ühikuteisendusi seadistada, väljal **Tootevariant**.

### <a name="product"></a>Toode

Kui valite valiku **Toode**, siis saate seadistada ühikuteisenduse tooteetaloni jaoks. See ühikuteisendus rakendub kõigile tootevariantidele ilma määratletud ühiku teisenduseta.

### <a name="example"></a>Näide

Tooteetalonil **T-särk** on neli väljastatud toodete varianti, S, M, L ja XL. T-särgid on pakendatud kastidesse ja ühes kastis võib olla viis t-särki, välja arvatud XL suurus, kus on ruumi ainult neljale t-särgile.

Avage kõigepealt lehekülg **Ühikuteisendus** toote **T-särk** väljastatut toote üksikasjade lehelt.

Seadistage lehel **Ühikuteisendus** ühikuteisendus väljastatud tootevariandi XL jaoks.

| **Väli**             | **Sätted**             |
|-----------------------|-------------------------|
| Loo teisendus: | Tootevariant         |
| Tootevariant       | T-särk : : XL : : |
| Lähteühik             | Kastid                   |
| Tegur                | 4                       |
| Ühikuks               | Osad                  |

Väljastatud toodete variantidel S, M ja L on ühikute Kast ja Tükid vahel sama ühikuteisendus, mis tähendab, et saate nende tootevariantide ühikuteisendused määratleda tooteetalonis.

| **Väli**             | **Sätted** |
|-----------------------|-------------|
| Loo teisendus: | Toode     |
| Toode               | T-särk     |
| Lähteühik             | Kastid       |
| Tegur                | 5           |
| Ühikuks               | Osad      |

### <a name="using-excel-to-update-the-unit-conversions"></a>Exceli kasutamine ühikuteisenduste värskendamiseks

Kui tootel on palju tootevariante erinevate ühikuteisendustega, on hea mõte eksportida ühikuteisendused leheküljelt **Ühikuteisendus** Exceli tabelisse, värskendada teisendusi ja seejärel laadida need tagasi rakendusse Supply Chain Mangement.

Excelisse eksportimise ja muudatuste uuesti rakendusse Supply Chain Mangementi laadimise valiku saab sisse lülitada lehekülje **Ühikuteisendus** tegumirea menüüelemendist **Ava Microsoft Office’is**.
