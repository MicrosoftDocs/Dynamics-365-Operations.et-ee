---
title: Käibemaksukoodide seadistamine
description: Selles teemas selgitatakse, kuidas seadistada käibemaksukoode rakenduses Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f6df5ed3fc49b537845e7d418d4953c0faee5f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994536"
---
# <a name="set-up-sales-tax-codes"></a>Käibemaksukoodide seadistamine

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
    - Kui päritolu välja kiirkaardil **Arvutused** on valitud summa üksuse kohta, korrutatakse väärtust kande kogusega, et arvutada käibemaksu summa.  Kui maksukood pole ühikupõhine maks, on väärtus protsent, mis rakendatakse selle maksukoodi päritolule käibemaksu summa arvutamiseks.     
11. Valige käsk **Salvesta**.
12. Sulgege leht.
13. Valige käsk **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]