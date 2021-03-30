---
title: Käibemaksu arvutamine ja korrigeerimine hankija arvel
description: Selles teemas selgitatakse, kuidas kohandada müügimaksu tarnija arvel rakenduses Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4d01fe7587e01c04af28be934a235d955455216
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204733"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Käibemaksu arvutamine ja korrigeerimine hankija arvel

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas kohandada müügimaksu tarnija arvel. Kui algne lähtedokument kuvab erinevad arvutatud maksusummade, saate neid summasid enne sisestamist korrigeerida. See ülesanne kasutab demoettevõtte DEMF andmeid.

1. Avage navigeerimispaanil **Moodulid > Ostureskontro > Arved > Arve tööleht**.
2. Valige suvand **Uus**.
3. Uue veeru väljal **Nimi** valige ripploendist suvand.
4. Toimingupaanil valige nupp **Alused**.
5. Täpsustage soovitud väärtusi väljal **Konto**.
6. Sisestage väärtus väljale **Arve**.
7. Sisestage number väljale **Kreedit**.
8. Määratlega väljal **Vastaskonto** soovitud väärtused.
9. Valige **Käibemaks**.
10. Sisestage number väljale **Tegeliku käibemaksu kogusumma**.
11. Vahekaardil **Korrigeerimine** saab korrigeerida käibemaksusummat käibemaksukoodi kohta.
12. Valige **Tegeliku väärtuse lähtestamine arvutatud summadest**.
13. Valige nupp **OK**.
14. Valige käsk **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]