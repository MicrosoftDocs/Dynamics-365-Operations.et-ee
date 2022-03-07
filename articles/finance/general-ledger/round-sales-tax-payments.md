---
title: Käibemaksu maksed ja ümardamisreeglid
description: See teema selgitab, kuidas toimib ümardamisreegli seadistus moodulis Käibemaksuhaldurid ja kuidas ümardada käibemaksusaldot töö Käibemaksu tasakaalustamine ja sisestamine käigus.
author: kailiang
ms.date: 10/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a75d41195875c5ed48cbe8ce5f5e448f173e718
ms.sourcegitcommit: 4f8465729d7ae0bf5150a2785a6140c984c7030e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2021
ms.locfileid: "7726796"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Käibemaksu maksed ja ümardamisreeglid

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas toimib ümardamisreegli seadistus moodulis Käibemaksuhaldurid ja kuidas ümardada käibemaksusaldot töö Käibemaksu tasakaalustamine ja sisestamine käigus.

Käibemaksu kohta tuleb perioodiliselt maksuametile aruandeid esitada ja see tasuda. Seda tegevust saab lõpetada, käivitades tasakaalustamise ja sisestades käibemaksuprotsessi lehel **Käibemaks**. Perioodi käibemaks tasakaalustatakse käibemaksukontodega ja käibemaksusaldo sisestatakse käibemaksu tasakaalustuskontole. Käibemaksusaldo, mis sisestatakse käibemaksu tasakaalustuskontole, saab maksuameti nõude järgi ümardada, seadistades lehel **Käibemaks** ümardamisreegli. 

Ümardamise erinevus sisestatakse käibemaksu ümardamise kontole, mis on valitud pearaamatus väljal Automaatsete kannete kontod.

Allolev näide selgitab lehel Käibemaksuhaldur ümardamisreegli toimimise põhimõtet.

## <a name="examples"></a>Näited

Perioodi kogu käibemaksu krediidisaldo on –98 765,43. Juriidiline isik kogus rohkem käibemaksu kui ise tasus. Seetõttu võlgneb juriidiline isik maksuametile raha. 

Juriidiline isik soovib kasutada ümardamismeetodit, mis ümardab saldo lähima täisarvuni (1,00). Käibemaksu arvestamise eest vastutav kasutaja peab tegema järgmist.

1. Klõpsake suvandeid **Maks** > **Kaudsed maksud** > **Käibemaks** > **Käibemaksuhaldurid**.
2. Valige kiirkaardi **Üldine** väljalt **Ümardamise vorm** suvand **Tavaline**.
3. Sisestage väljale **Ümardus** väärtus 1,00.
4. Kui saabub aeg tasuda maksuametile käibemaks, avage **Maks** > **Deklaratsioonid** > **Käibemaks** > **Käibemaksu tasakaalustamine ja sisestamine**. Käibemaksu tasakaalustamise kontol näete, et maksukohustuse summa **98 765,43** ümardatakse summale **98 765**.

Järgmine tabel näitab, kuidas ümardatakse summat 98 765,43, kasutades iga ümardusmeetodit, mis on saadaval lehe **Käibemaksuhaldurid** väljal **Ümardamise vorm**.

> [!NOTE]                                                                                  
> Kui ümardamisväärtuseks on seatud 0,00, siis kehtib järgmine.
>
> - Tavalise ümardamise puhul toimub ümardamine samamoodi nagu suvandi **Ümardus = 0,01** puhul.
> - Suvandite **Ümardamise vormi suvandid**, **Allapoole**, **Ülespoole ümardamine** ja **Oma kasuks** puhul käitutakse samamoodi nagu suvandi **Ümardus = 1,00** puhul.

| Ümardamise vormi suvand                | Ümardamisväärtus = 0,01 | Ümardamisväärtus = 0,10 | Ümardamisväärtus = 1,00 | Ümardamisväärtus = 100,00 | Ümardamisväärtus = 0,00   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| Tavaline                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                | 98,765.43                |
| Allapoole                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Ümardamine                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |
| Oma eelis kreeditsaldo puhul | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Oma eelis deebetsaldo puhul  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |

### <a name="normal-round-and-round-precision-is-001"></a>Tavaline ümardamine, ümardamistäpsus on 0,01

```<table>
  <tr>
    <td>Rounding
    </td>
    <td>Calculation process
    </td>
  </tr>
    <tr>
    <td>round(1.015, 0.01) = 1.02
    </td>
    <td>
      <ol>
        <li>round(1.015 / 0.01, 0) = round(101.5, 0) = 102
        </li>
        <li>102 * 0.01 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.014, 0.01) = 1.01
    </td>
    <td> <ol>
        <li>round(1.014 / 0.01, 0) = round(101.4, 0) = 101
        </li>
        <li>101 * 0.01 = 1.01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.011, 0.02) = 1.02
    </td>
    <td> <ol>
        <li>round(1.011 / 0.02, 0) = round(50.55, 0) = 51
        </li>
        <li>51 * 0.02 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.009, 0.02) = 1.00
    </td>
    <td> <ol>
        <li>round(1.009 / 0.02, 0) = round(50.45, 0) = 50
        </li>
        <li>50 * 0.02 = 1.00
        </li>
      </ol>
    </td>
  </tr>
</table>
```

> [!NOTE]                                                                                  
> Kui valite suvandi Oma eelis, toimub ümardamine alati juriidilise isiku kasuks. 

Lisateavet vt järgmistest teemadest:
- [Käibemaksu ülevaade](indirect-taxes-overview.md)
- [Käibemaksumakse loomine](tasks/create-sales-tax-payment.md)
- [Käibemaksukannete loomine dokumentidel](tasks/create-sales-tax-transactions-documents.md)
- [Sisestatud käibemaksukannete kuvamine](tasks/view-posted-sales-tax-transactions.md)
- [Ümardamisfunktsioon](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
