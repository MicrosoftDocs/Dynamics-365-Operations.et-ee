---
title: Kliendimaksete deponeerimine
description: Hoiustage kliendimaksed.
author: ShivamPandey-msft
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ed692d9c82fd496e31258a70415db1838d99313
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714029"
---
# <a name="deposit-customer-payments"></a>Kliendimaksete deponeerimine

[!include [banner](../../includes/banner.md)]

Hoiustage kliendimaksed. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Maksed > Maksete töölehed**.
2. Valige suvand **Uus**.
3. Väljal **Nimi** valige rippmenüüst **CustPay**.
4. Valige **Read**.
5. Väljal **Konto** valige klient, kelle jaoks registreerite makset.
6. Väljale **Kreedit** sisestage maksesumma. Saate valida summa tühjaks jätmise ja lasta selle süsteemil arvutada, valides makstud arved.  
7. Väljale **Makse viide** sisestage väärtus. Makse viiteks võib olla sisestatava makse tšeki number. Makse viide on vajalik makse kaasamiseks deposiitkviitungile.  
8. Märkige ruut Kasuta deposiitkviitungit. Kui makse tuleks deposiiti kaasata, muutke sätte väärtuseks Jah.  
9. Valige suvand **Uus**.
10. Väljal **Konto** valige klient järgmise makse jaoks.
11. Väljale **Kreedit** sisestage maksesumma.
12. Väljale **Makse viide** sisestage väärtus.
13. Märkige ruut **Kasuta deposiitkviitungit**.
14. Valige **Sisesta**. Maksed tuleb sisestada enne deposiitkviitungi loomist. See tagab, et maksed pärast deposiitkviitungi loomist ei muutuks.  
15. Valige **Funktsioonid**.
16. Valige **Deposiitkviitung**.
17. Valige nupp **OK**. Esimest lehte kasutatakse deposiitkviitungi loomiseks.  
18. Valige nupp **OK**. Teise etapina tuleb deposiitkviitung printida, kuid see etapp pole nõutav.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
