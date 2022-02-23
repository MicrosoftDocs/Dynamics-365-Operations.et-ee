---
title: Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul
description: See artikkel selgitab käibemaksukoodide välja Arvutusmeetod ja seda, kuidas käibemaksu vahemike ja terviksummade puhul arvutatakse.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3e18eac934eb109e8f3f509b2bd78f76dd5f74d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442369"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul

[!include [banner](../includes/banner.md)]

See artikkel selgitab käibemaksukoodide välja Arvutusmeetod ja seda, kuidas käibemaksu vahemike ja terviksummade puhul arvutatakse.

Saate seadistada käibemaksukoodi arvutamise kogusumma või intervallisumma põhjal. Valige käibemaksukoodi arvutamise viis lehe Käibemaksukoodid kiirkaardi Arvutamine väljal Arvutusmeetod.
- Kogusumma – maksumäära rakendatakse kogu maksustatavale summale.
- Intervall – maksustatav summa on jagatud osadeks, millest igaüks langeb kindla käibemaksumäärata vahemikku. Osa summast, mis langeb antud intervalli, maksustatakse selle intervalli maksumäära järgi. Käibemaks on iga summa intervalli kohta arvutatud maksusummade summa.
  > [!NOTE]                                                                                                                              
  > Suvand Intervall on saadaval ainult siis, kui valite lehel Pearaamatu parameetrid alal Käibemaks väljal Arvutusmeetod suvandi Rida. 

Intervallid seadistatakse lehel Käibemaksukood, sisestades iga maksumäära kohta alampiiri ja ülempiiri summad. Selleks et maksud arvutataks kõigi maksustatavate summade kohta olenemata valitud arvutusmeetodist, peavad intervallid järgima järgmisi reegleid.
-   Esimese intervalli alamlimiit peab olema null.
-   Viimase intervalli ülempiir peab olema null, mis tähistab lõpmatust.
-   Intervalli ülempiir peab olema järgmise intervalli alampiir.

Kui summa on eelmise intervalli ülempiir ja järgmise intervalli alampiir, rakendub summale esimese intervalli käibemaksumäär. Kui summa jääb väljapoole intervalle, mis on määratletud ülem- ja alampiiriga, rakendatakse käibemaksumäära null.

## <a name="example-whole-amount-method-of-calculation"></a>Näide. Arvutamismeetod: kogusumma
Lehel Käibemaksukoodid seadistatakse käibemaksumäärad järgmiste intervallidega.

|                   |                   |              |
|-------------------|-------------------|--------------|
| **Alampiir** | **Ülempiir** | **Maksumäär** |
| 0,00              | 50,00             | 30%          |
| 50,00             | 100,00            | 20%          |
| 100,00            | 0,00              | 10%          |

Käibemaks arvutatakse kogu maksustatava summa kohta.

| Maksustatav summa (hind) | Kalkulatsioon    | Käibemaks |
|------------------------|----------------|-----------|
| 35,00                  | 35,00 \* 0,30  | 10,50     |
| 50,00                  | 50,00 \* 0,30  | 15,00     |
| 85,00                  | 85,00 \* 0,20  | 17,00     |
| 305,00                 | 305,00 \* 0,10 | 30,50     |

## <a name="example-interval-method-of-calculation"></a> Näide. Arvutusmeetod: intervall
Lehel Väärtused seadistatakse käibemaksumäärad järgmiste intervallidega.

|                   |                   |              |
|-------------------|-------------------|--------------|
| **Alampiir** | **Ülempiir** | **Maksumäär** |
| 0,00              | 50,00             | 30%          |
| 50,00             | 100,00            | 20%          |
| 100,00            | 0,00              | 10%          |

Käibemaks on iga summa intervalli kohta arvutatud maksusummade summa.

| Maksustatav summa (hind) | Kalkulatsioon                                                               | Käibemaks |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | 10,50     |
| 50,00                  | 50,00 \* 0,30                                                             | 15,00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45.50     |



Lisateabe saamiseks vaadake teemat [Käibemaksumäärad väljade Marginaali alus ja Arvutusmeetod põhjal](marginal-base-field.md).





