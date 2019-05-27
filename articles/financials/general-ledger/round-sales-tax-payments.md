---
title: Käibemaksu maksed ja ümardamisreeglid
description: See artikkel selgitab, kuidas toimib ümardamisreegli seadistus moodulis Käibemaksuhaldurid ja kuidas ümardada käibemaksusaldot töö Käibemaksu tasakaalustamine ja sisestamine käigus.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1c1bb1c792eb79888a1df209f2eebaf14a38dd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1531853"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Käibemaksu maksed ja ümardamisreeglid

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas toimib ümardamisreegli seadistus moodulis Käibemaksuhaldurid ja kuidas ümardada käibemaksusaldot töö Käibemaksu tasakaalustamine ja sisestamine käigus.

Käibemaksu kohta tuleb perioodiliselt maksuametile aruandeid esitada ja see tasuda. Seda saab teha, käivitades tasakaalustamise ja sisestades käibemaksuprotsessi lehel Käibemaks. Perioodi käibemaks tasakaalustatakse käibemaksukontodega ja käibemaksusaldo sisestatakse käibemaksu tasakaalustuskontole. Käibemaksusaldo, mis sisestatakse käibemaksu tasakaalustuskontole, saab maksuameti nõude järgi ümardada, seadistades lehel Käibemaks ümardamisreegli. 

Ümardamise erinevus sisestatakse käibemaksu ümardamise kontole, mis on valitud pearaamatus väljal Automaatsete kannete kontod.

Allolev näide selgitab lehel Käibemaksuhaldur ümardamisreegli toimimise põhimõtet.

## <a name="examples"></a>Näited

Perioodi kogu käibemaksu krediidisaldo on –98 765,43. Juriidiline isik kogus rohkem käibemaksu kui ise tasus. Seetõttu võlgneb juriidiline isik maksuametile raha. 

Juriidiline isik soovib kasutada ümardamismeetodit, mis ümardab saldo lähima täisarvuni (1,00). Käibemaksu arvestamise eest vastutav kasutaja peab tegema järgmist.

1.  Klõpsake valikuid Maks &gt; Kaudsed maksud &gt; Käibemaks &gt; Käibemaksuhaldurid
2.  Valige kiirkaardi Üldine väljalt Ümardamise vorm suvand Tavaline.
3.  Sisestage väljale Ümardus väärtus 1,00.
4.  Kui saabub aeg tasuda maksuametile käibemaks, avage leht Käibemaksu tasakaalustamine ja sisestamine. (Klõpsake valikuid Maks &gt; Deklaratsioonid &gt; Käibemaks &gt; Käibemaksu tasakaalustamine ja sisestamine.)
5.  Käibemaksu tasakaalustamise kontol ümardatakse maksukohustuse summa 98 765,43 summale 98 765.

Järgmine tabel näitab, kuidas ümardatakse summat 98 765,43, kasutades iga ümardusmeetodit, mis on saadaval lehe Käibemaksuhaldurid väljal Ümardamise vorm.

| Ümardamise vormi suvand                | Ümardamisväärtus = 0,01 | Ümardamisväärtus = 0,10 | Ümardamisväärtus = 1,00 | Ümardamisväärtus = 100,00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| Tavaline                              | 98 765,43              | 98 765,40              | 98 765,00              | 98 800,00                |
| Allapoole                            | 98 765,43              | 98 765,40              | 98 765,00              | 98 700,00                |
| Ümardamine                         | 98 765,43              | 98 765,50              | 98 766,00              | 98 800,00                |
| Oma eelis kreeditsaldo puhul | 98 765,43              | 98 765,40              | 98 765,00              | 98 700,00                |
| Oma eelis deebetsaldo puhul  | 98 765,43              | 98 765,50              | 98 766,00              | 98 800,00                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a>Ümardamist pole, kui ümardamisväärtus on 0,00

round(1,0151, 0,00) = 1,0151 round(1,0149, 0,00) = 1,0149

### <a name="normal-round-and-round-precision-is-001"></a>Tavaline ümardamine, ümardamistäpsus on 0,01

<table>
  <tr>
    <td>Ümardamine
    </td>
    <td>Arvutamisprotsess
    </td>
  </tr>
    <tr>
    <td>round(1,015, 0,01) = 1,02
    </td>
    <td>
      <ol>
        <li>round(1,015 / 0,01, 0) = round(101,5, 0) = 102
        </li>
        <li>102 × 0,01 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1,014, 0,01) = 1,01
    </td>
    <td> <ol>
        <li>round(1,014 / 0,01, 0) = round(101,4, 0) = 101
        </li>
        <li>101 × 0,01 = 1,01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1,011, 0,02) = 1,02
    </td>
    <td> <ol>
        <li>round(1,011 / 0,02, 0) = round(50,55, 0) = 51
        </li>
        <li>51 × 0,02 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1,009, 0,02) = 1,00
    </td>
    <td> <ol>
        <li>round(1,009 / 0,02, 0) = round(50,45, 0) = 50
        </li>
        <li>50 × 0,02 = 1,00
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> Kui valite suvandi Oma eelis, toimub ümardamine alati juriidilise isiku kasuks. 

Lisateavet vt järgmistest teemadest:
- [Käibemaksu ülevaade](indirect-taxes-overview.md)
- [Käibemaksumakse loomine](tasks/create-sales-tax-payment.md)
- [Müügikannete loomine dokumentidel](tasks/create-sales-tax-transactions-documents.md)
- [Sisestatud käibemaksukannete kuvamine](tasks/view-posted-sales-tax-transactions.md)
- [Ümardamisfunktsioon](https://msdn.microsoft.com/en-us/library/aa850656.aspx)


