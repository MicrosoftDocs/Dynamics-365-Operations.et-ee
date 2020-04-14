---
title: Töölehe sisestuse loomine malli abil
description: Sisestatud töölehe kandeid saab salvestada Kande mallidena ja rakendada uue töölehe kandes.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 360df29e6349fd4d42d6d14af646e929b73943bd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145148"
---
# <a name="create-a-journal-entry-using-template"></a>Töölehe sisestuse loomine malli abil

[!include [banner](../../includes/banner.md)]

Sisestatud töölehe kandeid saab salvestada Kande mallidena ja rakendada uue töölehe kandes. See protsess kasutab demoettevõtte USMF-i andmeid.

1. Avage **Navigeerimispaan > Moodulid > Pearaamat > Töölehe kanded > Päevaraamatud**.
2. Paanil **Toimingupaan** klõpsake valikut **Uus**. See protseduur algab töölehe kande loomise ja sisestamisega, kuid varem sisestatud töölehe kannet saab salvestada mallina.  
3. Klõpsake väljal **Nimi** otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake **Read**.
7. Sisestage väärtus väljale **Konto liik**.
8. Sisestage väärtus väljale **Kirjeldus**.
9. Sisestage väärtus väljale **Deebet**.
10. Klõpsake valikut **Uus**.
11. Sisestage väärtus väljale **Konto liik**.
12. Sisestage väärtus väljale **Kirjeldus**.
13. Sisestage väärtus väljale **Deebet**.
14. Klõpsake valikut **Uus**.
14. Täpsustage soovitud väärtusi väljal **Konto**.
15. Sisestage väärtus väljale **Kirjeldus**.
16. Väljale **Kreedit** sisestage väärtus, et kanne tasakaalustada.
17. Paanil **Toimingupaan** klõpsake käsku **Sisesta**.
18. Klõpsake suvandit **Funktsioonid**.
19. Klõpsake malli **Salvesta kanne**.
20. Selle protseduuri eelduseks on tüüp **Protsendi mall**. Klõpsake nuppu OK.
    - Protsent: kogused kandes on teisendatud protsentuaalseteks teguriteks, mis lubab rakendamise igale kogusele, kui kande mall on valitud.
    - Kogus: tegelikud kogused talletatakse ja rakendatakse.  
21. Klõpsake **Pearaamatud**.
22. Klõpsake valikut **Uus**.
23. Klõpsake väljal **Nimi** otsingu avamiseks ripploendi nuppu.
24. Klõpsake loendis valitud real olevat linki.
25. Klõpsake **Read**.
26. Klõpsake suvandit **Funktsioonid**.
27. Klõpsake **Vali kande mall**.
28. Leidke varem loodud mall. Klõpsake valikut **OK**. Ehk peate klõpsama **Eelnev etapp** ja seejärel valima õige malli, kui on ka teisi malle.  
29. Sisestage kandele rakendatav summa väljale **Summa**. Väli **Summa** kuvatakse ainult siis, kui kande malli tüüp on Protsent.  
30. Klõpsake valikut **OK**.

