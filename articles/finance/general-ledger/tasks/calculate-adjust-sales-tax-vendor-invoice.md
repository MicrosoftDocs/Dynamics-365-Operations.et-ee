---
title: Käibemaksu arvutamine ja korrigeerimine hankija arvel
description: See teema kirjeldab, kuidas korrigeerida rakenduses Dynamics 365 Finance hankijaarve käibemaksu.
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d4d6a23f6f58906730c5ce00c5fe06885aaa6da
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734685"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Käibemaksu arvutamine ja korrigeerimine hankija arvel

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas kohandada müügimaksu tarnija arvel. Kui algne lähtedokument kuvab erinevad arvutatud maksusummade, saate neid summasid enne sisestamist korrigeerida. See ülesanne kasutab demoettevõtte DEMF andmeid.

1. Minge arve **töölehe > > ostureskontrole**.
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
