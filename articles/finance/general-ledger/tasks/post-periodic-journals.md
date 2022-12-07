---
title: Perioodiliste töölehtede sisestamine
description: Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse.
author: aprilolson
ms.date: 11/21/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdc1d9f67a515e3cdc45e173b88982feceb0ebfd
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799363"
---
# <a name="post-periodic-journals"></a>Perioodiliste töölehtede sisestamine

[!include [banner](../../includes/banner.md)]

Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse. Perioodilise töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu. Selles tegevuse juhises luuakse igakuise kordumismustriga perioodiline tööleht.

1. Avage **Navigeerimispaan > Moodulid > Pearaamat > Perioodilised ülesanded > Perioodilised töölehed**.
2. Klõpsake valikut **Uus**.
3. Sisestage või valige väärtus väljal **Nimi**.
4. Klõpsake loendis valitud real olevat linki.
5. Sisestage väärtus väljale **Kirjeldus**. See kirjeldus on hiljem ka perioodilise töölehe nimi, seetõttu tasub sellele anda asjakohane nimi.
6. Klõpsake paanil **Tegevuspaan** valikut **Read**. Perioodilisel töölehel on tavaliselt mitu töölehe rida. Ülesande juhend lisab siiski ainult ühe rea.
7. Väljale **Kuupäev** sisestage kuupäev. Väli **Kuupäev** sisaldab järgmise päevase töölehe kande sisestuskuupäeva. Iga kuu toodavad töölehed on soovitatav kasutada selle sisestamise kuu kuupäeva. See on tavaliselt perioodi esimene või viimane kuupäev. Kasutades välja **Tühi** kuupäev, saate jätta välja **Kuupäev** tühjaks ja anda töölehe toomiskuupäevaks kuupäeva. Välja väärtus uuendatakse kannete toomisel järgmisele korduvale kuupäevale. 
8. Täpsustage soovitud väärtusi väljal **Konto**.
9. Valige väärtus väljal **Kirjeldus**.
10. Sulgege leht.
11. Sisestage arv väljale **Deebet**.
12. Määratlega väljal **Vastaskonto** soovitud väärtused.
13. Valige **Kuud** väljal **Ühik**.
14. Ühikute **arvu väljale** sisestage **1**.
15. Sisestage kuupäev väljale **Lõpukuupäev**. Eelmise perioodi viimase kuupäeva sisestamine aitab vältida kogemata korduvtöölehe loomist valesse algusperioodi. Viimast kuupäeva värskendatakse hiljem iga kord, kui perioodilist töölehte tuuakse. 
16. Klõpsake valikut **Salvesta**.
17. Avage **Navigeerimispaan > Moodulid > Pearaamat > Töölehe kanded > Päevaraamatud**.
18. Klõpsake valikut **Uus**.
19. Sisestage või valige väärtus väljal **Nimi**.
20. Otsige loendist ja valige soovitud kirje.
21. Klõpsake loendis valitud real olevat linki.
22. Sisestage väärtus väljale **Kirjeldus**.
23. Klõpsake paanil **Tegevuspaan** valikut **Read**.
24. Paanil **Toimingupaan** klõpsake **Perioodiline tööleht**.
25. Klõpsake käsku **Too tööleht**.
26. Sisestage kuupäev väljale **Lõppkuupäev**. **Lõppkuupäev** toimib perioodiliste kannete ridadel nagu äralõikekuupäev. Kordumissätte, Viimase **kuupäeva** ja **Lõppkuupäeva** põhjal võib sama rida olla tulemuseks saadud töölehele kaasatud rohkem kui üks kord. Lõppkuupäeva **uuendatakse** automaatselt selle seansi kuupäeva alusel, mis on viimane kord, kui perioodiline rida töölehele üle kanti. 
27. Sisestage või valige väärtus väljal **Perioodilise töölehe kood**.
28. Klõpsake loendis valitud real olevat linki.
29. Klõpsake valikut **OK**. Sõltuvalt nõuetest ja seadistusest saab nüüd perioodi töölehte üle vaadata, kinnitada või sisestada.   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
