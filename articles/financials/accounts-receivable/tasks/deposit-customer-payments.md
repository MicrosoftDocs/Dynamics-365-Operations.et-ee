---
title: Kliendimaksete deponeerimine
description: Hoiustage kliendimaksed.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: afbf74d1cf3dc87e97dda0873115b5c7fa49ca3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834459"
---
# <a name="deposit-customer-payments"></a>Kliendimaksete deponeerimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Hoiustage kliendimaksed. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage Müügireskontro > Maksed > Makse tööleht.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
4. Valige makse tööleht. 
5. Klõpsake valikut Read.
6. Valige väljalt Konto klient, kelle puhul makse registreerite.
7. Sisestage makse summa väljale Kreedit.
    * Saate valida summa tühjaks jätmise ja lasta selle süsteemil arvutada, valides makstud arved.  
8. Sisestage väärtus väljale Makse viide.
    * Makse viiteks võib olla sisestatava makse tšeki number. Makse viide on vajalik makse kaasamiseks deposiitkviitungile.  
9. Märkige ruut Kasuta deposiitkviitungit.
    * Kui makse tuleks deposiiti kaasata, muutke sätte väärtuseks Jah.  
10. Klõpsake valikut Uus.
11. Valige järgmise makse klient väljalt Konto.
12. Sisestage maksesumma väljale Kreedit.
13. Sisestage väärtus väljale Makse viide.
14. Märkige ruut Kasuta deposiitkviitungit.
15. Klõpsake valikut Sisesta.
    * Maksed tuleb sisestada enne deposiitkviitungi loomist. See tagab, et maksed pärast deposiitkviitungi loomist ei muutuks.  
16. Klõpsake suvandit Funktsioonid.
17. Klõpsake suvandit Deposiitkviitung.
18. Klõpsake nuppu OK.
    * Esimest lehte kasutatakse deposiitkviitungi loomiseks.  
19. Klõpsake nuppu OK.
    * Teise etapina tuleb deposiitkviitung printida, kuid see etapp pole nõutav.  

