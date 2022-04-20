---
title: Saate häälestada käibemaksukoode.
description: See teema kirjeldab käibemaksukoodide seadistamist Dynamics 365 Finances.
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69e2cf9a16fe0e694154cccf9b49944b49c79b90
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565849"
---
# <a name="set-up-sales-tax-codes"></a>Saate häälestada käibemaksukoode.

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada käibemaksukoode. Käibemaksukoodid luuakse iga kaudse maksu või kohustuse puhul, mida juriidiline isik on kohustatud arvutama, koguma ja käibemaksuhalduritele maksma.

See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage **Navigeerimispaan > Maks > Kaudsed maksud > Käibemaks > Käibemaksukoodid**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Käibemaksukood**.
4. Sisestage väärtus väljale **Nimi**.
5. Valige ripploendit avades **Makseperiood**, et määrata, millisele maksumetile ja milliste intervallidega tuleb selle käibemaksu aruanded esitada ja maksud ära maksta.
6. Valige **Pearaamatusse kandmise grupp**, et määrata põhikontod käibemaksu pearaamatusse kandmiseks.
7. Laiendage kiirkaarti **Arvutused**. See sisaldab mitmeid välju, mis juhivad seda, kuidas käibemaksu summasid arvutatakse. Täitke need väljad vastavalt vajadusele.  
8. Valige liidese ülaosas **Toimingupaanil** valik **Käibemaksukood**.
9. Valige **Väärtused**.
10. Sisestage väärtus sellele käibemaksukoodile veerus **väärtus**.

    Kui **Päritolu** välja kiirkaardil **Arvutused** on valitud **Summa üksuse kohta** , korrutatakse väärtust kande kogusega, et arvutada käibemaksu summa.  Kui maksukood pole ühikupõhine maks, on väärtus protsent, mis rakendatakse selle maksukoodi päritolule käibemaksu summa arvutamiseks.     

11. Valige käsk **Salvesta**.
12. Sulgege leht.
13. Valige käsk **Salvesta**.

Microsoft Dynamics Finantsversiooni 365 10.0.22 [...](../../localizations/global-tax-calcuation-service-overview.md)[**·**](../../localizations/emea-multiple-vat-registration-numbers.md)**puhul**, kui kasutate maksuteenust ja funktsioonihalduse tööruumis on lubatud mitme käibemaksu registreerimisnumbri toe funktsioon, **saate** maksukoodi tüübi määramiseks kasutada maksuvälja Tüüpi. Saadaval on järgmised väärtused:

- Standardne KM
- Alandatud KM
- KM 0%
- Aktsiis
- Muud

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
