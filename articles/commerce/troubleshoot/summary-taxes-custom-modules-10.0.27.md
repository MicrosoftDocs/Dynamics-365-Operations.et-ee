---
title: Tellimuse kokkuvõtte vahesumma ei sisalda makse, kui kasutatakse kohandatud tellimuse kokkuvõttemooduleid
description: See artikkel annab tõrkeotsingu juhised, mis aitavad teil kasutada kohandatud tellimuse kokkuvõtte mooduleid ja tellimuse kokkuvõtte vahesumma ei sisalda tasude makse stsenaariumis "hind sisaldab käibemaksu".
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 260dcb6bc1585615195e32adfcd1da6bfbca294e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848833"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Tellimuse kokkuvõtte vahesumma ei sisalda makse, kui kasutatakse kohandatud tellimuse kokkuvõttemooduleid

See artikkel annab tõrkeotsingu juhised, mis aitavad teil kasutada kohandatud tellimuse kokkuvõtte mooduleid ja tellimuse kokkuvõtte vahesumma ei sisalda tasude makse stsenaariumis "hind sisaldab käibemaksu".

## <a name="description"></a>Kirjeldus

Microsoft Dynamics 365 Commerce Versiooni 10.0.27 väljalaskest on tehtud järgmised muudatused stsenaariumis "hind sisaldab käibemaksu", et pakkuda järjepidevat kogemust tellimuse koondmoodulites e-ärisaidi lehtedel.

- Lisatud on kaks uut välja: **TaxOnShippingCharge** ja **TaxOnNonShippingCharges**.
- Rakenduste **GetSalesOrderBySalesId** **ja GetSalesOrderByTransactionId** rakenduse programmeerimisliidesed (API-d) on täpsed väärtused järgmistele väljadele stsenaariumis "hind sisaldab käibemaksu":

    - VahesummaSalesAmount
    - VahesummaAmountWithoutTax
    - Vahesumma
    - ShippingChargeAmount
    - MuuchargeAmount

Kuid kui kasutate kohandatud tellimuse kokkuvõtte mooduleid, võivad need muudatused mõjutada tellimuse koondkokkuvõtte väärtusi, mitte kaasates tasude makse.

## <a name="resolution"></a>Lahendus

Kui kasutate kohandatud tellimuse kokkuvõtte mooduleid ja ei soovi tuletada kaubandusversiooni 10.0.27 ja uuemates stsenaariumites "hind sisaldab käibemaksu" tehtud muudatusi, järgige selle jaotise juhiseid.

Pöördudes tagasi eelmise (enne versiooni 10.0.27) **salesTransaction.SubtotalAmount ja salesTransaction.SubtotalAmountWithoutTax** **·**, taastate kogukulu maksusumma (**TaxOnShippingCharge** **ja TaxOnNonShippingCharges**) kaasamise vahesummasse (**SubtotalAmount** ja **SubtotalAmountWithoutTax).**

Eelmise tellimuse koondkäitumise tagasipöördumiseks järgige neid samme.

1. Avage Commerce Headquartersis commerce'i parameetrite leht (**Rakenduse Retail ja Commerce \> Headquarters häälestamise \> parameetrid \> Äriparameetrid**).
1. Valige vasakul navigeerimispaanil **konfiguratsiooni parameetrid**.
1. Lisage järgmised konfiguratsiooniparameetrid ja seadke iga parameetri väärtus **tõestele**:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - Väljad IsLegacyOrderSummaryAasiationEnabled

> [!NOTE]
> Kui olete eelnevalt kasutanud **konfiguratsiooniparameetrit IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** **ja soovite tellimusele säilitada sama käitumise. Atribuut NetAmountWithoutTax** peaksite lisama ka konfiguratsiooniparameetri IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled **ja** selle väärtuse väärtuseks **tõene**.

## <a name="additional-resources"></a>Lisaressursid

[Maksude jaotuse teabe peitmine tellimuse kokkuvõtetes](../hide-taxes-breakup.md)
