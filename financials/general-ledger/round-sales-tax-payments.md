---
title: "Käibemaksu maksed ja ümardamisreeglid"
description: "See artikkel selgitab, kuidas toimib ümardamisreegli seadistus moodulis Käibemaksuhaldurid ja kuidas ümardada käibemaksusaldot töö Käibemaksu tasakaalustamine ja sisestamine käigus."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7ec117598a6a008e5b274179659b515824029874
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="sales-tax-payments-and-rounding-rules"></a>Käibemaksu maksed ja ümardamisreeglid

[!include[banner](../includes/banner.md)]


See artikkel selgitab, kuidas toimib ümardamisreegli seadistus moodulis Käibemaksuhaldurid ja kuidas ümardada käibemaksusaldot töö Käibemaksu tasakaalustamine ja sisestamine käigus.

Käibemaksu kohta tuleb perioodiliselt maksuametile aruandeid esitada ja see tasuda. Seda saab teha, käivitades tasakaalustamise ja sisestades käibemaksuprotsessi lehel Käibemaks. Perioodi käibemaks tasakaalustatakse käibemaksukontodega ja käibemaksusaldo sisestatakse käibemaksu tasakaalustuskontole. Käibemaksusaldo, mis sisestatakse käibemaksu tasakaalustuskontole, saab maksuameti nõude järgi ümardada, seadistades lehel Käibemaks ümardamisreegli. 

Ümardamise erinevus sisestatakse käibemaksu ümardamise kontole, mis on valitud pearaamatus väljal Automaatsete kannete kontod.

Allolev näide selgitab lehel Käibemaksuhaldur ümardamisreegli toimimise põhimõtet.

### <a name="example"></a>Näide:

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
| Tavaline                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                |
| Allapoole                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                |
| Ümardamine                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                |
| Oma eelis kreeditsaldo puhul | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                |
| Oma eelis deebetsaldo puhul  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                |

> [!NOTE]                                                                                  
> Kui valite suvandi Oma eelis, toimub ümardamine alati juriidilise isiku kasuks. 

Lisateavet leiate jaotisest [Käibemaksu ülevaade](indirect-taxes-overview.md). 




