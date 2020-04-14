---
title: Perioodiliste töölehtede sisestamine
description: Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7f721a05c8b74f1cfcf43177b73129751483650e
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144932"
---
# <a name="post-periodic-journals"></a>Perioodiliste töölehtede sisestamine

[!include [banner](../../includes/banner.md)]

Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse. Perioodilise töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu. Selles tegevuse juhises luuakse igakuise kordumismustriga perioodiline tööleht.

1. Avage **Navigeerimispaan > Moodulid > Pearaamat > Perioodilised ülesanded > Perioodilised töölehed**.
2. Klõpsake valikut **Uus**.
3. Sisestage või valige väärtus väljal **Nimi**.
4. Klõpsake loendis valitud real olevat linki.
5. Sisestage väärtus väljale **Kirjeldus**. See kirjeldus on hiljem ka perioodilise töölehe nimi, seetõttu tasub sellele anda asjakohane nimi.
6. Klõpsake paanil **Tegevuspaan** valikut **Read**. Perioodilisel töölehel on tavaliselt mitu töölehe rida. Selles ülesandes lisatakse sellele siiski vaid üks rida.
7. Väljale **Kuupäev** sisestage kuupäev. Väli **Kuupäev** sisaldab järgmise päevase töölehe kande sisestuskuupäeva. Igakuiste töölehtede puhul on soovitatav kasutada kuupäeva, mil see sisestatakse, tavaliselt kas esimene viimane kuupäev perioodis. Kasutades välja Tühi kuupäev võite jätta välja Kuupäev tühjaks ning lisada selle siis, kui tööleht on toodud. Välja värskendatakse automaatselt järgmise korduva kuupäevani, kui kandeid tuuakse. 
8. Täpsustage soovitud väärtusi väljal **Konto**.
9. Valige väärtus väljal **Kirjeldus**.
10. Sulgege leht.
11. Sisestage arv väljale **Deebet**.
12. Määratlega väljal **Vastaskonto** soovitud väärtused.
13. Valige Kuud väljal **Ühik**.
14. Sisestage number 1 väljale **Ühikute arv**.
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
26. Sisestage kuupäev väljale **Lõppkuupäev**. **Lõppkuupäev** toimib perioodiliste kannete ridadel nagu äralõikekuupäev. Olenevalt kordussätetest võivad samal real paiknevad Viimane kuupäev ja Lõpukuupäev esineda tulemuseks oleval töölehel rohkem kui ühel korral. Lõpukuupäeva värskendatakse automaatselt olenevalt perioodilise rea viimase töölehele ülekandmise seansi kuupäevast. 
27. Sisestage või valige väärtus väljal **Perioodilise töölehe kood**.
28. Klõpsake loendis valitud real olevat linki.
29. Klõpsake valikut **OK**. Sõltuvalt nõuetest ja seadistusest saab nüüd perioodi töölehte üle vaadata, kinnitada või sisestada.   
